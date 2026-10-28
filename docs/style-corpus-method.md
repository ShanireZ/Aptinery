---
type: procedure
title: shanirez-style corpus measurement method
description: Reproducing the measured claims in SKILL.md against the OJCode corpus.
tags: [style, corpus, verification]
status: stable
---

# shanirez-style corpus measurement method

Every statistic in `plugins/shanirez-style/skills/shanirez-style/SKILL.md` is
measured against the [OJCode corpus](https://github.com/ShanireZ/OJCode).
Do not add, soften or strengthen a claim without re-running the count. From
a local clone of that corpus:

```bash
git ls-files '*.cpp' > /tmp/all.txt
git log --diff-filter=A --since="<2 years ago>" --name-only --format="" -- '*.cpp' \
  | grep -v '^$' | sort -u > /tmp/added.txt
while IFS= read -r f; do [ -f "$f" ] && printf '%s\n' "$f"; done \
  < /tmp/added.txt > /tmp/recent.txt
xargs -a /tmp/recent.txt -d '\n' grep -lIE '<pattern>' | wc -l
```

- `--diff-filter=A` alone is not the recent set; intersect it with files that still exist.
- Where a habit shifted, the last two years win.
- State whether a percentage is whole-corpus or recent.
- Use `xargs -a <list> -d '\n'`; filenames contain spaces.
- Grep before asserting a name or the absence of a form.
