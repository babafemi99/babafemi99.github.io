# Portfolio + Notes

Static portfolio and blog. Plain HTML/CSS, no build step.

## Structure

```
/
  index.html              Homepage (portfolio)
  /blog
    index.html            Notes index
    five-cent-heist.html
    forgotten-machine.html
  /assets
    styles.css            Shared tokens / base styles
  .nojekyll               Tells GitHub Pages to serve files as-is
```

## Run locally

Open `index.html` in a browser, or:

```bash
npx serve .
```

## Deploy on GitHub Pages

1. Create a repo on GitHub and push this directory.
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio + notes"
   git branch -M main
   git remote add origin git@github.com:<you>/<repo>.git
   git push -u origin main
   ```
2. In the repo: **Settings → Pages → Build and deployment**.
3. Source: **Deploy from a branch** → Branch: **main** → Folder: **/ (root)** → Save.
4. Wait ~1 minute. Site goes live at `https://<you>.github.io/<repo>/`.

For a custom domain, add a `CNAME` file at the root containing the domain, then point DNS at GitHub Pages.

## Add a new note

1. Copy one of the existing posts in `/blog/` as a template.
2. Update `<title>`, the post-meta number, the headline, and the body.
3. Add a link to it in `/blog/index.html` and (optionally) the Notes section of `/index.html`.

## Notes

- Original source HTML is preserved in `/html/` for reference.
- Each page currently ships its own `<style>` block tuned to its layout. `assets/styles.css` is where shared tokens live for future consolidation.
