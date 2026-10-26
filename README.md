# Gran Rally Racing

A single-file browser rally game (three.js). Everything (cars, music, textures) is embedded in `index.html`; three.js and Google Fonts load from CDNs, so players need an internet connection.

## Deploy to Vercel
1. Push this folder to a GitHub repo.
2. On vercel.com choose **Add New → Project**, import the repo.
3. Framework Preset: **Other**. Leave build command and output directory empty. Click **Deploy**.

(CLI alternative: `npm i -g vercel && vercel --prod` in this folder.)

## Deploy to GitHub Pages
1. Create a repo and push these files to the `main` branch.
2. In the repo go to **Settings → Pages → Source: GitHub Actions**.
3. The included workflow publishes the site at `https://<user>.github.io/<repo>/`.

## Notes
- The game is split into `parts/part1-3.txt` (about 11 MB each) so every file stays under GitHub's 25 MB web-upload limit. `index.html` is a tiny loader that downloads and joins them. Keep the `parts` folder next to `index.html`.
- To upload on github.com: **Add file -> Upload files**, drag in `index.html`, `vercel.json`, `.nojekyll`, `README.md` and the whole `parts` folder. Upload `.github` separately via the same dialog (or use GitHub Desktop / git, which allow files up to 100 MB).
- three.js and Google Fonts load from CDNs, so players need an internet connection.
- Credits: check the license of the Lancia Stratos model pack before publishing publicly.
