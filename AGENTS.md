# AGENTS.md — Aptinery

In a containing workspace, also read its `../AGENTS.md` when present.

Aptinery is an Agent Skills marketplace. GitHub `ShanireZ/Aptinery` is the
development authority; the machine identifier is `aptinery`.

## Read before editing

- [CONTRIBUTING.md](CONTRIBUTING.md) owns packaging, invocation, source-preservation
  and verification contracts. Read it before changing skills or distribution files.
- [NOTICE](NOTICE) owns pinned sources, attribution, license limits and intentional
  adaptations. Read the applicable section and package notices before editing
  imported material. A repository license declaration does not grant rights to
  third-party material.
- [docs/style-corpus-method.md](docs/style-corpus-method.md) owns the method for
  `shanirez-style` statistics. Recompute before changing a measured claim.
- [INSTALL.md](INSTALL.md) owns installation and skill-specific runtime requirements.

## Change boundaries

Keep plugin IDs, synchronized manifest versions, skill paths and invocation
policies consistent. Preserve fixed upstream copies and licenses byte-for-byte
except for adaptations explicitly documented in NOTICE. The three Claude source
mirrors are distribution adapters, not additional products.

Write Aptinery-authored documentation in English. Retain upstream language,
source titles and domain-specific output examples where preservation requires it.
Keep machine settings, publication approvals, investigation logs and temporary
execution records outside the repository. Record reusable source and license
facts in NOTICE, and reusable contributor rules in CONTRIBUTING.md.

## Verification

Run `git diff --check` from the repository root for every change. Parse all JSON
manifests and YAML metadata; validate names, versions, paths, skill discovery,
explicit invocation policies, local links and license files. Compare unchanged
vendor trees with their pinned upstream objects and report unavailable objects
as unverified. See CONTRIBUTING.md for client-check prerequisites and limits.

This is a distribution package with no application-level build/test command.
Use [GitHub Issues](https://github.com/ShanireZ/Aptinery/issues) for project work.
