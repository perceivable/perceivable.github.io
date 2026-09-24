# perceivable.github.io

Public site for Perceivable. Two pages, no build step, no external requests.

| Path | Served at | Purpose |
| --- | --- | --- |
| `index.html` | `/` | Product page for A11yScope — used as the homepage URL in the Chrome Web Store listing |
| `privacy/index.html` | `/privacy/` | Privacy policy — **required** by the Web Store dashboard |

## Setup

GitHub Pages, source: `main` branch, `/` (root).

## House rule

Both pages must pass A11yScope itself with zero violations. A tool that sells
accessibility from an inaccessible website has nothing to sell.

```bash
# from the a11yscope working copy
node tools/scan.mjs ../site/index.html
node tools/scan.mjs ../site/privacy/index.html
```

Current status: 31/31 checks passed on both.
