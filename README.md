# Tools

A small collection of self-contained browser tools, hosted on GitHub Pages.

**Live:** https://berigor.github.io/hpage/

| Page | Live | Source |
| --- | --- | --- |
| Landing page | [`/`](https://berigor.github.io/hpage/) | `index.html` |
| Floor Planner | [`/floor-planner/`](https://berigor.github.io/hpage/floor-planner/) | `floor-planner/index.html` |
| Wheel of Fortune | [`/wheel-of-fortune/`](https://berigor.github.io/hpage/wheel-of-fortune/) | `wheel-of-fortune/index.html` |

## Adding a page

GitHub Pages serves the repo as a plain file tree, so a new page is just a new
directory with an `index.html` in it — no config, no build step, no router:

```
mkdir my-tool
$EDITOR my-tool/index.html    # becomes /my-tool/
```

Then add a card for it in the root `index.html`. Each page is a single
self-contained HTML file with no external dependencies, so pages never
interfere with each other.

## Running locally

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

Serve from the repo root rather than opening files directly, so the relative
links between pages resolve the way they do in production.

## Deployment

Pushes to `master` are deployed by `.github/workflows/deploy.yml`, which
uploads the whole tree.

One-time setup: in the repo's **Settings → Pages**, set **Source** to
**GitHub Actions**.
