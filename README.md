# Room Plan Editor

Draw a single-room floor plan and arrange furniture with intuitive drag-and-drop, right in the browser.

**Live:** https://berigor.github.io/floorplanner/

## Running locally

The app is one self-contained HTML file with no build step and no external dependencies — open `index.html` in a browser, or serve it:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Pushes to `master` are deployed to GitHub Pages by `.github/workflows/deploy.yml`.

One-time setup: in the repo's **Settings → Pages**, set **Source** to **GitHub Actions**.
