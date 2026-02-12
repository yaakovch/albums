# Albums Project

## Repo
- GitHub: `yaakovch/albums`
- GitHub Pages: `https://yaakovch.github.io/albums/`

## How to create and deploy a new album

When the user adds a new WhatsApp export folder and asks to "deploy" or "create" an album:

### Phase 1: Data Analysis & Curation
1. **Find the chat log** — recursively search the folder for `_chat.txt` files
2. **Parse chat history** — analyze the last 12 months of messages
3. **Identify events** — find significant moments (birthdays, trips, holidays) based on media frequency and chat intensity
4. **Select photos** — curate 30–50 representative photos from the folder
5. **Extract quotes** — find real messages/reactions associated with each photo to use as captions

### Phase 2: Build the Album HTML
6. **Generate a single HTML file** — e.g. `<name>_album.html` in the repo root
   - Masonry grid layout with lightbox
   - Vertical timeline of events
   - Real quotes as stylized speech bubbles
   - Minimalist, mobile-responsive design with Tailwind CSS via CDN
   - All media paths relative (initially pointing to the source folder)

### Phase 3: Deploy to GitHub Pages
7. **Create a dedicated image folder** — e.g. `album_<name>/` with only the images referenced in the HTML (not the full source folder)
8. **Update the HTML** — replace source folder paths with the new `album_<name>/` paths
9. **Update `.gitignore`** — add an exception like `!album_<name>/*.jpg`
10. **Commit and push** — stage the HTML, image folder, and `.gitignore`, then push to `main`
11. **GitHub Pages** — site auto-deploys from `main`. The album will be at `https://yaakovch.github.io/albums/<filename>.html`

## Family context
- **Yaakov** — father (the user)
- **Sapir** — mother/wife
- **Ruti** — older daughter
- **Noga** — younger daughter
Use this context to attribute quotes and label events accurately.

## Existing albums
- `family_album_2025.html` → images in `album/` → https://yaakovch.github.io/albums/family_album_2025.html

## Notes
- `.gitignore` blocks `*.jpg` (and other media) by default — each album image folder needs an explicit exception
- Keep album image folders small (only referenced images, not full source folders)
- The original detailed prompt template is in `claude_code_prompt.md` for reference
