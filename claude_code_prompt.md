# Claude Code Prompt: Family Year in Review Album

Act as a Senior Full-Stack Developer and Data Analyst.

## Context
I have a WhatsApp export (chat logs and media) stored in subfolders within this "albums" directory.

## Goal
Create a "Year in Review" digital photo album as a single-file, responsive HTML/CSS/JS application.

## Tasks

### 1. Data Analysis
- Recursively search subfolders for `_chat.txt` files and media files (JPG, PNG, MP4).
- Parse the chat history from the last 12 months.
- Analyze the frequency of media shares and chat intensity to identify significant "Events" (e.g., birthdays, trips, holidays).
- Identify which photos correspond to specific chat conversations using filenames referenced in the text.

### 2. Curation
- Select 30–50 representative photos from the last year.
- For each selected photo, find the original message sent with it or the immediate reactions following it.
- Extract real quotes from group members to use as captions/descriptions.

### 3. Contextual Knowledge
- **The family members in this group are:** Sapir (wife), and our daughters Ruti and Noga.
- Use this context to attribute quotes and label events accurately.

### 4. Frontend Design
- Use your **Frontend Design Skill** to create a modern, elegant web gallery.
- **Features:** Masonry grid layout, lightbox for viewing photos, and a vertical timeline of events.
- **Style:** Minimalist, mobile-responsive, with smooth CSS transitions. Include the extracted quotes as stylized "speech bubbles" or captions next to the relevant images.
- Use **Tailwind CSS via CDN** for styling to ensure a high-end look without extra local dependencies.

## Output
- Generate a file named `family_album_2025.html` in the root directory.
- Ensure all media paths in the HTML are relative so the file is portable.
