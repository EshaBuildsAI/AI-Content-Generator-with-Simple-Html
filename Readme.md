# AI Content Generator

A free, single-file web app that generates emails, cover letters, WhatsApp messages, and LinkedIn posts — in a tone of your choice (Formal, Friendly, or Professional). Powered by Google's Gemini API (free tier).

## Features

- **4 content types:** Email, Cover Letter, WhatsApp Message, LinkedIn Post
- **3 tones:** Formal, Friendly, Professional
- **Optional recipient/role field** for more tailored output
- **Copy to clipboard** and **regenerate** buttons
- Clean, dark, corporate-style UI
- 100% free — no paid API, no backend, no database
- Runs entirely in the browser — your API key is stored only in your own browser (`localStorage`) and is sent directly to Google, never to any third-party server

## Tech Stack

- Plain **HTML + CSS + JavaScript** (single file — no build tools, no frameworks)
- **Google Gemini API** (`gemini-2.5-flash` model) for content generation

## Getting Started

### 1. Get a free Gemini API key
1. Go to [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Click **Create API Key** — no credit card required

### 2. Run the app

Because this app calls Google's API directly from the browser, it needs to be served over `http://` or `https://` rather than opened directly as a file (`file://`), otherwise you may see a "Failed to fetch" error.

**Option A — Local server (quick test):**
```bash
python3 -m http.server 8000
```
Then open `http://localhost:8000` in your browser.

**Option B — Deploy for free (recommended):**
- **GitHub Pages:** Push this repo to GitHub → Settings → Pages → select `main` branch → get a free live link
- **Netlify:** Drag and drop the `index.html` file at [netlify.com](https://netlify.com) for an instant live link
- **Vercel / Cloudflare Pages:** Connect your GitHub repo for automatic free deployment

### 3. Use the app
1. Open the deployed link (or local server link)
2. Click **Add API key** (top right) and paste your Gemini API key → **Save key**
3. Choose a **content type** and **tone**
4. Optionally add a recipient/role
5. Describe what the content should be about
6. Click **Generate draft**
7. Use the **copy** icon to copy the result, or **regenerate** for a new draft

## Notes

- Your API key never leaves your browser except to go directly to Google's servers.
- The free Gemini tier has daily/per-minute request limits. If you hit a quota error, wait a bit and try again, or check current limits at [ai.google.dev/pricing](https://ai.google.dev/pricing).
- No data is stored on any server — everything is generated and displayed in real time.

## License

Free to use and modify for personal or commercial projects.