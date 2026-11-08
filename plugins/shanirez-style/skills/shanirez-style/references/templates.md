# Verified algorithm templates (ShanireZ OJ style)

Canonical forms in the author's current hand. Each follows the house style: Allman braces,
4-space indent, **no blank lines**, 1-based indexing, global allocation, short names, `cin`/`cout`
with `endl`, explicit `long long`. Copy the shape, not just the idea — including the density.

Contents:
1. DSU and Kruskal (`g[]` + `find`)
2. Closed-interval binary search
3. Fenwick tree (`lowbit`)
4. Lazy segment tree (`lc/rc` node pool)
5. Graph storage (`to[]` unweighted, `es[]` weighted)
6. Dijkstra (`priority_queue` + `vector<Edge>`)
7. Binary-lifting LCA (recursive DFS build)
8. Grid BFS (`struct Node` queue, `ms[4][2]`, `nx`/`ny`)
9. Sorting structs (`operator<` and `cmp`)
10. Multi-test-case scaffold

---

## 1. DSU and Kruskal

The parent array is `g[]`, the root finder is `find` with path compression in one line, and
`g[i] = i` is set while reading. A merge happens inline with the comma operator. Kruskal keeps a
flat `vector<Edge> es;`, sorts it with a by-value `cmp`, and walks it with range-for.

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
struct Edge
{
    int u, v, w;
};
vector<Edge> es;
int n, m, cnt, g[100005];
long long ans;
bool cmp(Edge a, Edge b)
{
    return a.w < b.w;
}
int find(int x)
{
    return g[x] = (x == g[x] ? x : find(g[x]));
}
int main()
{
    cin >> n >> m;
    for (int i = 1; i <= n; i++)
    {
        g[i] = i;
    }
    for (int i = 1; i <= m; i++)
    {
        int u, v, w;
        cin >> u >> v >> w;
        es.push_back(Edge{u, v, w});
    }
    sort(es.begin(), es.end(), cmp);
    for (Edge e : es)
    {
        int gu = find(e.u), gv = find(e.v);
        if (gu != gv)
        {
            g[gu] = gv, ans += e.w, cnt++;
        }
    }
    cout << (cnt == n - 1 ? ans : -1) << endl;
    return 0;
}
```

---

## 2. Closed-interval binary search

Search on `[l, r]`; the answer is `r` after the loop. The decision is a one-line ternary, and
`mid` is a plain local.

```cpp
while (l <= r)
{
    long long mid = (l + r) / 2;
    check(mid) ? l = mid + 1 : r = mid - 1;
}
cout << r << endl;
```

---

## 3. Fenwick tree

```cpp
long long c[100005];
int lowbit(int x)
{
    return x & -x;
}
void edit(int x, long long k)
{
    while (x <= n)
    {
        c[x] += k;
        x += lowbit(x);
    }
}
long long query(int x)
{
    long long ans = 0;
    while (x)
    {
        ans += c[x];
        x -= lowbit(x);
    }
    return ans;
}
```

---

## 4. Lazy segment tree (node pool with `lc/rc`)

The house segment tree is a **static struct pool** `ns` with an allocation counter and explicit
`lc/rc` child links (never `now << 1`). The builder `init` takes the child slot by reference; the
range update is `edit`. `mid` is recomputed as a local in each function. Child links stay `int`;
only value fields widen to `long long`. This is range-add / range-sum.

```cpp
#define MX 100005
struct Node
{
    int lc, rc;
    long long v, tag;
};
Node ns[MX * 4];
int n, m, root, pos;
long long a[MX];
void init(int &now, int l, int r)
{
    now = ++pos;
    if (l == r)
    {
        ns[now].v = a[l];
        return;
    }
    int mid = (l + r) / 2;
    init(ns[now].lc, l, mid), init(ns[now].rc, mid + 1, r);
    ns[now].v = ns[ns[now].lc].v + ns[ns[now].rc].v;
}
void pushdown(int now, int l, int r)
{
    if (ns[now].tag)
    {
        int mid = (l + r) / 2;
        ns[ns[now].lc].v += (mid - l + 1) * ns[now].tag;
        ns[ns[now].rc].v += (r - mid) * ns[now].tag;
        ns[ns[now].lc].tag += ns[now].tag;
        ns[ns[now].rc].tag += ns[now].tag;
        ns[now].tag = 0;
    }
}
void edit(int now, int l, int r, int x, int y, long long k)
{
    if (x <= l && y >= r)
    {
        ns[now].v += (r - l + 1) * k;
        ns[now].tag += k;
        return;
    }
    pushdown(now, l, r);
    int mid = (l + r) / 2;
    if (x <= mid)
    {
        edit(ns[now].lc, l, mid, x, y, k);
    }
    if (y > mid)
    {
        edit(ns[now].rc, mid + 1, r, x, y, k);
    }
    ns[now].v = ns[ns[now].lc].v + ns[ns[now].rc].v;
}
long long query(int now, int l, int r, int x, int y)
{
    if (x <= l && y >= r)
    {
        return ns[now].v;
    }
    pushdown(now, l, r);
    int mid = (l + r) / 2;
    long long ans = 0;
    if (x <= mid)
    {
        ans += query(ns[now].lc, l, mid, x, y);
    }
    if (y > mid)
    {
        ans += query(ns[now].rc, mid + 1, r, x, y);
    }
    return ans;
}
// build with: init(root, 1, n);
```

---

## 5. Graph storage

An adjacency `vector` named for its payload: `to` when the element is the neighbour, `es` when it
is an `Edge` record. Push with `push_back`; walk with range-for unless the edge index matters, and
then cast the bound: `for (int i = 0; i < (int)es[now].size(); i++)`.

```cpp
// unweighted
vector<int> to[100005];
to[u].push_back(v), to[v].push_back(u);
for (int nxt : to[now])
{
    // visit nxt
}
// weighted or carrying extra data
struct Edge
{
    int to, w;
};
vector<Edge> es[100005];
es[u].push_back(Edge{v, w}), es[v].push_back(Edge{u, w});
for (Edge e : es[now])
{
    // e.to, e.w
}
```

---

## 6. Dijkstra

Lazy Dijkstra: a min-heap via a reversed `operator<` on a small `Path` struct, a `0x3f` whole-array
fill, and each node finalized the first time it is popped.

```cpp
#include <algorithm>
#include <cstring>
#include <iostream>
#include <queue>
#include <vector>
using namespace std;
struct Edge
{
    int to, w;
};
struct Path
{
    int v, w;
    bool operator<(const Path &oth) const
    {
        return w > oth.w;
    }
};
vector<Edge> es[100005];
priority_queue<Path> q;
int n, m, s, dis[100005];
int main()
{
    cin >> n >> m >> s;
    for (int i = 1; i <= m; i++)
    {
        int u, v, w;
        cin >> u >> v >> w;
        es[u].push_back(Edge{v, w});
    }
    memset(dis, 0x3f, sizeof(dis));
    q.push(Path{s, 0});
    while (q.size())
    {
        int now = q.top().v, d = q.top().w;
        q.pop();
        if (dis[now] != 0x3f3f3f3f)
        {
            continue;
        }
        dis[now] = d;
        for (Edge e : es[now])
        {
            if (dis[e.to] == 0x3f3f3f3f)
            {
                q.push(Path{e.to, d + e.w});
            }
        }
    }
    for (int i = 1; i <= n; i++)
    {
        cout << dis[i] << " ";
    }
    cout << endl;
    return 0;
}
```

---

## 7. Binary-lifting LCA

A **recursive DFS**, not a BFS. The doubling row of `now` is filled at the top of `dfs`, because
its parent's row is already complete. Depth is `h[]`; the parent is skipped with `from`.
`anc[i][j]` is the 2^j-th ancestor of `i`; the literal height 19 covers n ≤ 5e5.

```cpp
vector<int> to[500005];
int n, h[500005], anc[500005][20];
void dfs(int now, int from)
{
    for (int i = 1; i <= 19; i++)
    {
        anc[now][i] = anc[anc[now][i - 1]][i - 1];
    }
    for (int nxt : to[now])
    {
        if (nxt == from)
        {
            continue;
        }
        anc[nxt][0] = now, h[nxt] = h[now] + 1;
        dfs(nxt, now);
    }
}
int lca(int a, int b)
{
    if (h[a] < h[b])
    {
        swap(a, b);
    }
    for (int i = 19; i >= 0; i--)
    {
        if (h[anc[a][i]] >= h[b])
        {
            a = anc[a][i];
        }
    }
    if (a == b)
    {
        return a;
    }
    for (int i = 19; i >= 0; i--)
    {
        if (anc[a][i] != anc[b][i])
        {
            a = anc[a][i], b = anc[b][i];
        }
    }
    return anc[a][0];
}
// root it with: h[1] = 1, dfs(1, 0);
```

---

## 8. Grid BFS

Offsets live in a global `ms[4][2]`; the candidate cell is `nx`/`ny`. The queue carries a
two-field `struct Node` pushed as `Node{x, y}`. The bounds, wall and visited checks merge into one
`||` guard. The grid is a 0-based `string s[]` read with `cin >> s[i]`.

```cpp
struct Node
{
    int x, y;
};
queue<Node> q;
string s[1005];
int n, m, dis[1005][1005], vis[1005][1005];
int ms[4][2] = {{0, 1}, {0, -1}, {1, 0}, {-1, 0}};
void bfs(int sx, int sy)
{
    q.push(Node{sx, sy}), vis[sx][sy] = 1;
    while (q.size())
    {
        int x = q.front().x, y = q.front().y;
        q.pop();
        for (int i = 0; i < 4; i++)
        {
            int nx = x + ms[i][0], ny = y + ms[i][1];
            if (nx < 0 || nx >= n || ny < 0 || ny >= m || s[nx][ny] == '#' || vis[nx][ny])
            {
                continue;
            }
            vis[nx][ny] = 1, dis[nx][ny] = dis[x][y] + 1;
            q.push(Node{nx, ny});
        }
    }
}
```

---

## 9. Sorting structs

A natural order is a member `operator<` by const reference with the parameter `oth`. A one-off
order, or several orders over the same data, is a free comparator taking its arguments by value.

```cpp
struct Node
{
    int x, y;
    bool operator<(const Node &oth) const
    {
        return x == oth.x ? y < oth.y : x < oth.x;
    }
};
Node ns[100005];
sort(ns + 1, ns + n + 1);
// several orders over the same data
struct Cake
{
    int id, v;
};
Cake cs[100005];
bool cmpid(Cake a, Cake b)
{
    return a.id == b.id ? a.v > b.v : a.id < b.id;
}
bool cmpv(Cake a, Cake b)
{
    return a.v > b.v;
}
sort(cs + 1, cs + n + 1, cmpid);
```

---

## 10. Multi-test-case scaffold

```cpp
int main()
{
    int T;
    cin >> T;
    while (T--)
    {
        // solve one case; reset reused globals here
    }
    return 0;
}
```

When the case number is part of the output, index the loop instead:

```cpp
for (int t = 1; t <= T; t++)
{
    int ans = 1e9;
    // solve one case
    cout << "Case #" << t << ": " << (ans == 1e9 ? -1 : ans) << endl;
}
```
