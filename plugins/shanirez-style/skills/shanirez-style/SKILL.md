---
name: shanirez-style
description: >-
  ShanireZ's personal C++14 competitive-programming / online-judge coding style. Use whenever the
  user wants C++ for an algorithm or online-judge problem — pasting a problem statement, asking to
  solve it or explain it with code, naming a judge problem id (Luogu P*/B*, CodeForces CF*, LOJ #*,
  PAT, AtCoder ABC*/ARC*/AGC*, SPOJ SP*, UVa UVA*), or asking to write, debug, optimize, or
  refactor an existing .cpp in the OJCode workspace. Read this first so the code matches the
  author's own hand (Allman braces, 4-space indent, no blank lines, 1-based, global state, terse
  names, cin/cout with endl, explicit long long). Do NOT use for general-purpose C++ engineering
  (GUI/Qt apps, servers/networking, embedded, build systems, library/API design, business-logic
  debugging) or for non-C++ tasks — those are not OJCode solutions.
---

# ShanireZ OJ Style (shanirez-style)

## What this is

A fingerprint of the author's **current** hand, measured on the `OJCode` corpus: the **313
single-file solutions added between 2025-11-08 and 2026-11-08 that still exist** (309 under
`Luogu/`, 4 under `SP UVA AT/`). Every "N of 313" below counts files in that set. Habits that have
dropped out of the last year are deliberately left out of this file; when you edit an older
solution, keep whatever that file already does instead of modernizing it.

Solutions are throwaway scripts: one file, one problem, global state, terse names, no build
system, no abstraction layers. Resist the instinct to "engineer" them — no OOP wrappers, no
namespaces of your own, no reusable templates, no exceptions, no logging, no test scaffolding.

The dialect is **C++14**. The reference build is
`g++ -std=c++14 -O2 -Wall -m64 -static-libgcc -fexec-charset=UTF-8 -Wl,-stack=1073741824`, so don't
reach for C++17/20 library features. The **1 GB stack** belongs to that environment and is why tree
algorithms stay recursive; check the target judge's stack budget before relying on deep recursion.

---

## The skeleton

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int n, m, ans, a[100005];
int main()
{
    cin >> n >> m;
    for (int i = 1; i <= n; i++)
    {
        cin >> a[i];
    }
    cout << ans << endl;
    return 0;
}
```

- **Explicit headers, alphabetically sorted.** `<iostream>` (311 of 313) and `<algorithm>` (310)
  are in almost every file; add `<vector>` (65), `<queue>` (33), `<cstring>` (15), `<iomanip>`
  (11), `<map>` (10), `<cmath>` (8) as needed. No `<bits/stdc++.h>` (1 of 313) and no `<cstdio>`.
- **`using namespace std;`** in every file (313 of 313).
- **Globals right after the headers**: arrays, structs, scalars, then helper functions, then
  `int main()`. Helpers (`dfs`, `find`, `query`, `check`…) are free functions above `main`.
- **`int main()`** (never `signed main()`), ending in `return 0;` (313 of 313). No `#pragma`.

---

## I/O — fixed rules

These are the owner's rules, not measurements; they hold even where an old file does otherwise.

- **Read with `cin`, write with `cout`.** Never `scanf`, `printf`, `getchar`, `putchar`, or a
  hand-written `read()` / `write()`.
- **No stream tuning.** Never write `ios::sync_with_stdio(false)`, `cin.tie(0)`, `cout.tie(0)`,
  `cin.tie(0)->sync_with_stdio(false)` or any variant.
- **Every line ends with `endl`** — never `'\n'` or `"\n"`. A row of values is
  `cout << a[i] << " ";` inside the loop and `cout << endl;` after it.
- **Choices go inline:** `cout << (ok ? "Yes" : "No") << endl;`
- **Formatted floats:** `cout << fixed << setprecision(2) << ans << endl;` with `<iomanip>`
  (10 of 313).
- **Multiple test cases:** `int T; cin >> T; while (T--) { ... }` (25 files; 6 use `t`). Use
  `for (int t = 1; t <= T; t++)` only when the case number is printed (`"Case #" << t << ": "`).
- **Input until EOF:** `while (cin >> n)`.

---

## Formatting

### Where it comes from

The layout is what `clang-format` produces under the VS Code C/C++ extension's *Visual Studio*
fallback style: **Allman braces, 4-space indent, `SortIncludes` on, `ColumnLimit: 0`**.

- **Includes are always sorted** — 313 of 313 files.
- **There is no column limit.** Longest-line percentiles: p50 = 53, p90 = 80, p99 = 112,
  max = 155. A long condition or `cout` chain stays on one line; never wrap to fit a ruler.

### Allman braces — always, on every block

The opening `{` goes on its own line for functions, structs, loops and conditionals, and braces
are **never omitted**, even for a one-statement `if`/`for`/`while`/`else`. No K&R line and no
brace-less body appears anywhere in the 313 files.

```cpp
if (gu != gv)
{
    g[gu] = gv, cnt++;
}
```

### Indentation: 4 spaces in a new file

249 of 313 files use 4 spaces. The 64 tab-indented files are a burst from one editor setup — 55 of
them were added between 2025-11 and 2026-01, and only 9 of the 221 files since 2026-02 use tabs.
**New file → 4 spaces. Editing a file → keep its existing indentation**; never mix the two or
reindent a whole file.

### No blank lines, no final newline

A solution is one solid block: 312 of 313 files contain no blank line — not between headers and
globals, not between functions, not inside them. The last byte is the closing `}` of `main`, with no
trailing newline (312 of 313).

---

## Arrays, variables and naming

- **Large arrays are global**, sized with a margin as an inline literal: `int a[100005];`,
  `long long sum[500005];`. `#define MX 500005` (9 of 313) is the only macro form, used when one
  bound appears many times. Never `const int maxn`, `typedef`, or `#define int long long` (0 each).
- **Pack related globals on one line**, initializers included:
  `long long n, m, ans = 1, base = 233, mod = 1e9 + 7, h1[200005];`
- **A modulus is a global variable `mod`** on that line (`mod = 1e9 + 7`, 8 files), not a macro.
  A string-hash base is `base = 233` (5 files).
- **Containers are global too**: every one of the 32 files with a `queue` or `priority_queue`
  declares it at file scope (`queue<Node> q;`, `priority_queue<Path> q;`), and `string s;` is
  global in 22 files against 6 local. Clear a reused global between test cases.
- **Short, traditional names:**
  - sizes and counts: `n m k q T`; loop indices `i j`, with `k` for a genuine third index such as
    Floyd's middle vertex. Index names follow the array dimension (`anc[i][j]`), not nesting order.
  - graph: `u v w` for an edge; **`to`** for an unweighted adjacency list, **`es`** for
    `vector<Edge>`; **`now`** for the current node and **`nxt`** for the neighbour.
  - tree depth `h[]` (11 files, against 6 for `dep[]`); parent `fa[]` when it is stored.
  - accumulators `ans cnt tot sum res`; state `vis dis dp f pos id`; intervals `l r mid`.
  - flags are `int`, not `bool`: `int ok = 1; ... ok = 0;` (`trig` occasionally) — 15 files use
    an `int` flag and none declares a `bool` variable.
  - structs are PascalCase — **`Node` (27 files), `Edge` (14), `Path` (6)** — with terse fields
    (`x y`, `to w`, `u v w`, `lc rc v tag`). The global array of a struct is **`ns`**
    (`Node ns[100005];`).
- **`long long` is written out** (104 of 313 files). If a few variables share one short
  declaration line, make the whole line `long long`. When many big arrays are involved, widen only
  the value-carrying ones and keep indices, depths, ids and flags `int`.

### Indexing: 1-based by default

`for (int i = 1; i <= n; i++)` outnumbers `for (int i = 0; i < n; i++)` 519 to 59. Arrays are used as
`a[1..n]` and sorted with `sort(a + 1, a + n + 1)`. Use 0-based indexing only for natively 0-based
data — string characters, bitmask bits, a `string s[]` grid — and cast `.size()` to `int` in loop
bounds.

---

## Idioms that make it look authentic

- **Comma operator for tightly related updates on one line:**
  ```cpp
  g[gu] = gv, ans += e.w, cnt++;
  vis[nx][ny] = 1, dis[nx][ny] = dis[x][y] + 1;
  ```
- **Inline ternaries** (73 of 313 files), as a statement or inside output:
  ```cpp
  check(mid) ? l = mid + 1 : r = mid - 1;
  cout << (ans == 1e9 ? -1 : ans) << endl;
  ```
- **Infinity is a literal.** `1e9` (27 files) and `1e18` (12), assigned and compared directly. To
  fill a whole array use `memset(dis, 0x3f, sizeof(dis))` (9 files, `<cstring>`) and compare against
  `0x3f3f3f3f`. Never `INT_MAX`, `LLONG_MAX` or `#define INF` (0).
- **Compute a shared prerequisite once, then merge guard clauses with `||`** rather than a
  staircase of early exits:
  ```cpp
  int l = lca(x, y);
  if (a[x] == 0 || z[x] + z[y] - 2 * z[l] > 0)
  {
      cout << "Yes" << endl;
      continue;
  }
  ```
- **Emptiness is `.size()`, never `.empty()`** (0 of 313): `while (q.size())`, `if (v.size())`.
- **Graph storage is an adjacency `vector` named for its payload**: `vector<int> to[100005]`
  (17 files) when the element is the neighbour, `vector<Edge> es[100005]` (10) when it is an edge
  record, and a flat `vector<Edge> es;` for an edge list that gets sorted (Kruskal). Push with
  `push_back` (60 files; `emplace_back` 0). Walk it with range-for:
  `for (int nxt : to[now])`, `for (Edge e : es[now])`.
- **A tree DFS carries its parent instead of using `vis[]`:** `void dfs(int now, int from)` and
  `if (nxt == from) continue;` first thing in the loop (8 files). When the parent is needed later,
  store it in `fa[]` and skip `nxt == fa[now]`.
- **Grid moves use a global `ms[4][2]` table and `nx`/`ny`**, never `dx`/`dy`. The grid is usually a
  0-based `string s[1005]`, so bounds read `nx < 0 || nx >= n`.
- **DSU is `g[]` plus `find`** with path compression, merged inline:
  `int gu = find(u), gv = find(v); if (gu != gv) { g[gu] = gv, cnt++; }`.
- **One function with a parameter, not near-duplicates**: `val(x, 2)` / `val(x, 5)`, not
  `val2` / `val5`.
- **No redundant casts.** Cast only when the whole expression would otherwise be evaluated narrow
  (`(long long)a * b` with two `int`s).
- **Sorting.** A struct with one natural order gets a member
  `bool operator<(const T &oth) const` (17 of the 24 files that define one use exactly this
  signature). A one-off order, or several orders over the same data, gets a free comparator that
  takes its arguments by value: `bool cmp(Edge a, Edge b)`, or `cmpid` / `cmpv` side by side.
  Sort 1-based ranges (`sort(ns + 1, ns + n + 1, cmp)`) or a flat vector
  (`sort(es.begin(), es.end(), cmp)`). **No lambdas** (0 of 313); `auto` is essentially unused (1).
- **Priority queues**: a min-heap of structs reverses `operator<`; a min-heap of scalars is
  `priority_queue<int, vector<int>, greater<int>> q;`.

---

## Comments

Sparse — 31 of 313 files have any. A short Chinese (UTF-8) note for a non-obvious step or a
derivation, usually **trailing on the same line** (52 trailing lines against 20 standalone). No
block comments (`/* */`, 0 files). Don't narrate the code line by line, and don't append a tag or
signature line after `main`.

---

## File placement and naming

- Put the file in its judge folder: `Luogu/`, `CodeForces/`, `LOJ/`, `PAT/Basic/`,
  `PAT/Advanced/`, `SP UVA AT/`.
- Name it by the **exact problem id**: `P3372.cpp`, `B4339.cpp`, `T777250.cpp`, `CF1009F.cpp`,
  `#10000.cpp`, `ABC403G.cpp`, `UVA10079.cpp`, `SP1043.cpp`.
- For an alternative approach or a partial solution, append a space and a suffix:
  `P3367 Dfn.cpp`, `P3372 Zkw.cpp`, `P9753 90pts.cpp`.

---

## Verified algorithm templates

For a standard structure or algorithm, use the forms in
[`references/templates.md`](references/templates.md) — DSU and Kruskal, closed-interval binary
search, Fenwick tree, lazy segment tree, graph storage, Dijkstra, binary-lifting LCA, grid BFS,
struct sorting and the multi-test scaffold. They already follow every rule above; copy the shape,
including the density.

---

## Don't do these

- `scanf`, `printf`, `getchar`, `putchar`, a hand-written `read()`/`write()`, or any
  `sync_with_stdio` / `cin.tie` / `cout.tie` line.
- `'\n'` or `"\n"` as a line terminator — always `endl`.
- Blank lines anywhere, or a newline after the final `}`.
- Wrapping long lines, or an include block out of alphabetical order.
- `#include <bits/stdc++.h>` or `<cstdio>`.
- K&R braces, or a brace-less one-line `if`/`for`/`while`/`else`.
- Tabs in a new file.
- `#define int long long`, `typedef long long ll`, `const int maxn`, `#define mid`, `#define MOD`,
  `#define INF`, `INT_MAX`/`LLONG_MAX` — use explicit `long long`, inline bounds (or `#define MX`),
  a global `mod` variable and `1e9`/`1e18`.
- `while (!q.empty())` — write `while (q.size())`.
- `emplace_back`, lambdas, `auto`, `pair`-based queues, or chained-forward-star edge arrays.
- `dx`/`dy` — the table is `ms[4][2]`, the target cell `nx`/`ny`.
- `bool` flags with long names (`isFound`, `parentArray`) — `int ok`, `fa`, `now`.
- Wrapping an algorithm in a class, namespace or reusable template.
