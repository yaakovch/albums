# Albums Project

## Repo
- GitHub: `yaakovch/albums`
- GitHub Pages: `https://yaakovch.github.io/albums/`

## How to deploy a new album page

When asked to deploy/publish an album HTML file:

1. **Identify images** — find all image paths referenced in the HTML (e.g. `home_stuff/...`)
2. **Create a dedicated folder** — e.g. `album_<name>/` with only the referenced images (not the full source folder)
3. **Update the HTML** — replace old paths with the new folder paths
4. **Update `.gitignore`** — add an exception like `!album_<name>/*.jpg` so the images get tracked
5. **Commit and push** — commit the HTML, images, and `.gitignore` change, then push to `main`
6. **GitHub Pages** — the site auto-deploys from `main` branch. Remind the user to enable Pages if not already enabled.

## Existing albums
- `family_album_2025.html` → images in `album/` → https://yaakovch.github.io/albums/family_album_2025.html

## Notes
- `.gitignore` blocks `*.jpg` by default — each album folder needs an explicit exception
- Keep album image folders small (only referenced images, not full source folders)
