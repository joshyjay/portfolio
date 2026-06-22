# Joshua Anani — Portfolio

A static personal portfolio site. No build step. `index.html` and `styles.css` in the repo root, assets in `media/`.

Built from `portfolio_master.md`, which is the content and design contract.

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

No build step is required. The files are served exactly as they are.

1. Create a repository and push this folder to the `main` branch.
   ```bash
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Select branch **main** and folder **/ (root)**, then **Save**.
5. The site goes live at `https://<you>.github.io/<repo>/` within a minute or two.

The included `.nojekyll` file tells GitHub Pages to serve the files verbatim, so the numbered assets in `media/` are delivered untouched.

## Notes

- Media is referenced by number (`media/1`, `media/3`, and so on). The active set is 1 to 7, 10, 11, 12, 14. Numbers 8, 9, 13, 15 are intentionally absent.
- Videos play muted, looping, inline. `media/6.mp4` uses `media/5.png` as its poster.
- The design follows section 5 of `portfolio_master.md`. The site is responsive, keyboard accessible, and respects reduced motion.
