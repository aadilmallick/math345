# Math345 — Static Demo Site

Dear professor Mainak,

This small repository contains demo pages for a course assignment, including an interactive SIR model visualization.

Files of interest:

- `index.html` — landing page and navigation
- `sir-charts.html` — interactive SIR model visualization (Chart.js + Tailwind)

## Deploy to GitHub Pages

You can host this site on GitHub Pages (static hosting). Two common options:

1. Serve from the `main` (or `master`) branch (root):

   - In your GitHub repo, go to Settings → Pages.
   - Under "Source", select the branch (e.g. `main`) and folder `/(root)`.
   - Save. Your site will be available at `https://<username>.github.io/<repository>/`.

2. Serve from a `gh-pages` branch (recommended if you want a separate deployment branch):

   - From your local project, you can create and publish the `gh-pages` branch with these commands:

```bash
# build/prepare (not needed for pure static files)
# create gh-pages branch and push current contents
git checkout --orphan gh-pages
git --work-tree=. add --all
git --work-tree=. commit -m "Publish to gh-pages"
git push origin gh-pages --force
git checkout -f main
```

   - Then in GitHub Settings → Pages, select `gh-pages` as the source.

## Routing notes

- All links in the site are relative. This ensures the pages work whether served at the repository root or a subpath like `/<repo>/`.
- The `index.html` includes a `<base href="./">` to further help relative routing.

If you want, I can also add a small GitHub Action to automatically publish on push to `main` or `gh-pages`.

---
Made with ❤️ — ready to deploy to GitHub Pages.
