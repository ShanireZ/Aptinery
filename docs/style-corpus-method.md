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
Do not add, soften or strengthen a claim without re-running the count. The
current figures use the files added in the year before 2026-11-08 that still
exist (313 files). From a local clone of that corpus:

```bash
git log --diff-filter=A --since="<1 year ago>" --name-only --format="" -- '*.cpp' \
  | grep -v '^$' | sort -u > /tmp/added.txt
while IFS= read -r f; do [ -f "$f" ] && printf '%s\n' "$f"; done \
  < /tmp/added.txt > /tmp/recent.txt
xargs -a /tmp/recent.txt -d '\n' grep -lIE '<pattern>' | wc -l
```

- `--diff-filter=A` alone is not the recent set; intersect it with files that still exist.
- The skill describes the last year only. Drop a habit that no longer appears there
  instead of documenting it as legacy; editing guidance for older files is
  "keep what the file already does".
- Counts are files in the recent set unless the text says lines or loops.
- Use `xargs -a <list> -d '\n'`; filenames contain spaces.
- Grep before asserting a name or the absence of a form.
- The I/O section (`cin`/`cout` only, no stream tuning, `endl` on every line) is an
  owner rule, not a measurement; do not weaken it from corpus counts.
