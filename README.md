<div align="center">

<img width="720" height="720" alt="Picsart_26-10-16_21-15-23-480" src="https://github.com/user-attachments/assets/9dbd45bf-c7e0-4042-b31c-3c227a8c6a86" />

### A quiet space to write.

<p>A lightweight, local-first Markdown editor for notes, ideas, and everything in between.</p>

<p>
  <img alt="HTML" src="https://img.shields.io/badge/HTML5-static-242424?style=flat-square&logo=html5&logoColor=white">
  <img alt="CSS" src="https://img.shields.io/badge/CSS3-custom-242424?style=flat-square&logo=css3&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-vanilla-242424?style=flat-square&logo=javascript&logoColor=white">
  <img alt="No build step" src="https://img.shields.io/badge/build-no%20build%20step-242424?style=flat-square">
</p>

[Explore the source](https://github.com/aabhro/Still) · [Open `Still.html`](https://github.com/aabhro/Still/blob/main/Still.html)

</div>

---

## Overview

**Still** is a browser-based writing space built with plain HTML, CSS, and JavaScript. It combines a distraction-light editor with a practical notes library, live Markdown preview, linked notes, and optional AI writing tools.

There is no framework, package manager, or build process. Your notes are saved in your browser, and you can export them whenever you need a portable copy.

## Features

### Writing

- **Markdown editor and live preview** with headings, emphasis, lists, quotes, links, inline code, code blocks, dividers, tables, and images.
- **Formatting palette** for common Markdown actions without memorising the syntax.
- **Typewriter mode** keeps the active line near the centre of the editor.
- **Writing preferences** for font, text size, line spacing, and workspace width.
- **Live writing statistics** for word count, character count, and estimated reading time.
- **Find and replace** for quick edits across the current note.

### Notes library

- Create, rename, and delete notes, and organise them into folders.
- Keep multiple notes open with editor tabs and use the **Quick Switcher** to move between them.
- Add tags, pin important notes, and mark favourites. Filter the library by title, content, folder, or tag.
- Start from templates for essays, meeting notes, study notes, journals, and task lists.
- Create a date-based daily note for quick journaling or daily planning.
- Browse automatic version history and restore an earlier snapshot.

### Linked notes

- Link notes with wiki-style links such as `[[Reading list]]`.
- Follow links to existing notes or create a note when a link does not exist yet.
- Explore relationships in an interactive graph, and inspect incoming backlinks and outgoing references.

### Personalisation

Choose from four themes:

- **Monochrome** ; near-black, minimal surfaces.
- **Editorial**  ; warm, paper-inspired tones.
- **ChatGPT**    ; clean, light interface.
- **Google**     ; a bright, neutral interface.

Theme and writing preferences are remembered in the current browser.

### Import, export, and backup

- Export the current note as **Markdown (`.md`)** or **plain text (`.txt`)**.
- Export your notes library, folders, open tabs, and version history as a **JSON backup**.
- Restore a backup by merging it with the current library or replacing the library.
- Import Markdown (`.md`, `.markdown`) and plain-text (`.txt`) files. The library importer also accepts JSON backups (`.json`).

### Optional Gemini writing assistant

Still includes an optional AI writer powered by Google's Gemini API. Add your own API key, select a model, and generate or revise text from a prompt. You can choose to include the current note as context, and review generated edits before accepting them.

AI features are optional. The rest of the editor does not require a Gemini key.

## Getting started

### Run locally

1. Clone or download this repository.

   ```bash
   git clone https://github.com/aabhro/Still.git
   cd Still
   ```

2. Open `Still.html` in a modern browser.

For the most reliable local setup, serve the folder over localhost instead of opening the file directly:

```bash
python -m http.server 8000
```

Then visit **http://localhost:8000/Still.html**.

No `npm install`, compilation, or build command is required.

### Deploy

Still is a static website, so it can be hosted on GitHub Pages, Netlify, or another static host. Deploy the project files together and open `Still.html` at the deployed URL. To make the site root load Still automatically, rename or copy the entry file to `index.html` and check that the referenced manifest, icons, and service worker remain at the expected paths.

The HTML references `manifest.webmanifest`, `sw.js`, `icon.svg`, and `apple-touch-icon.png`. Installable-app and service-worker behaviour depends on serving the app over HTTPS or localhost and having the referenced companion files available.

## Keyboard shortcuts

Still uses a shortcut chord to keep everyday typing uninterrupted. Press **Shift + F2**, release the keys, then press the command key.

| Shortcut | Action |
| --- | --- |
| `Shift + F2`, then `N` | Create a note |
| `Shift + F2`, then `M` | Open the formatting palette |
| `Shift + F2`, then `B` / `I` / `K` | Bold / italic / insert link |
| `Shift + F2`, then `P` | Toggle Markdown preview |
| `Shift + F2`, then `T` | Toggle typewriter mode |
| `Shift + F2`, then `Q` | Open Quick Switcher |
| `Shift + F2`, then `V` | Open version history |
| `Shift + F2`, then `L` | Open graph view and backlinks |
| `Shift + F2`, then `A` | Open the Gemini writer |
| `Shift + F2`, then `R` | Open find and replace |
| `Shift + F2`, then `D` | Open today's daily note |
| `Shift + F2`, then `C` | Open the command palette |
| `Alt + ↓` | Open the formatting palette from the editor |
| `Tab` | Indent the current selection |
| `Esc` | Close the current menu or dialog |

The in-app help panel lists additional commands and formatting options. Type `help` in the editor to open it.

## Storage and privacy

- **Local-first notes:** notes, folders, preferences, tabs, and version history are stored in the browser's local storage for the current site. They are not automatically synced between browsers or devices.
- **Back up your library:** clearing browser/site data can remove locally stored notes. Export a JSON library backup regularly and keep it somewhere safe.
- **Gemini requests:** when you use the AI writer, your prompt is sent to Google's Gemini API. If you enable current-note context, the current note is sent as part of that request too.
- **API key storage:** the Gemini key is saved in local storage in your browser and is used directly by the client to call Google's API. Avoid saving a personal key on shared devices or exposing it in a publicly distributed copy of the app.
- **External assets:** the page loads DM Sans and DM Mono from Google Fonts.

## Built with

| Technology | Role |
| --- | --- |
| HTML5 | App structure |
| CSS | Layout, themes, responsive styling, and motion |
| Vanilla JavaScript | Editing, note management, Markdown rendering, and local persistence |
| Browser Local Storage | Notes, preferences, and version history |
| Google Gemini API | Optional AI-assisted writing |

---

<div align="center">

**Write a little. Keep what matters.**

Made to stay out of the way.

</div>
