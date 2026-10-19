# BrowserForge 🔨

BrowserForge is a zero-setup AI IDE and Native Web Agent that runs in your browser. It allows you to mount a local workspace, edit code, view documents, and leverage various flagship AI models to autonomously perform file operations right on your machine.

## ✨ Features
* **Zero Backend:** No server component — the UI runs in your browser. UI libraries (Monaco, Tailwind, SheetJS, Mammoth, marked) are loaded from CDNs, so an internet connection is required at load time. Your workspace files stay local.
* **Multi-Provider AI:** Built-in support for OpenAI, Google Gemini, Anthropic Claude, xAI, Mistral, DeepSeek, local models via Ollama/LM Studio, and more.
* **Smart File Editor:** Integrated [Monaco Editor](https://microsoft.github.io/monaco-editor/) with syntax highlighting.
* **Document Support:** Preview images and PDFs, read Excel (`.xlsx`) files, and parse Word (`.docx`) documents natively.
* **Voice Dictation:** Speak your prompts directly to the agent.
* **Privacy First:** API keys stay in the browser. When you send a prompt, the file tree and the content of the currently open non-secret file are sent to the selected AI provider — secret files (`.env`, `*.pem`, keys, credentials) are excluded automatically.

## 🚀 How to Use
1. Clone the repository or simply open `index.html` in a modern browser (Chrome/Edge recommended for File System API support).
2. Click **Mount Workspace** and select a local folder to work in.
3. Configure your preferred **Provider Preset**, model, and API Key in the top navigation bar.
4. Open a file from the left sidebar or prompt the agent in the bottom chat area to create, modify, or delete files autonomously!

## ⚠️ Requirements & Known Limitations
* **Internet connection required at load:** UI libraries are loaded from CDNs (Tailwind, Monaco, marked, SheetJS, Mammoth, Font Awesome). If any fail to load, a red banner explains which features are unavailable; the file tree, chat and PDF preview keep working. Fully offline use requires vendoring the assets locally (see below).
* **Browser support:** Mounting a workspace requires the [File System Access API](https://developer.chrome.com/articles/file-system-access/) — available in Chromium browsers (Chrome/Edge). Other browsers show a hint in the chat instead. Voice dictation uses the Web Speech API (Chrome).
* **Data sharing:** The system prompt sent to your provider contains the workspace file tree and the content of the currently open non-secret file (see "Privacy First" above). Files marked as secrets are withheld automatically.
* **Mobile:** On screens narrower than 768 px the file explorer becomes a slide-in drawer — tap the ☰ button in the header to open it.
* **Offline use (vendoring):** to make the app work fully offline, download the following assets into a local `vendor/` folder and replace the CDN URLs in `index.html`:
  * Tailwind CSS (standalone build), Monaco Editor `min/vs` bundle, require.js, marked, SheetJS (`xlsx.full.min.js`), Mammoth (`mammoth.browser.min.js`), Font Awesome CSS+webfonts.

## 🛠️ Tech Stack
* HTML5 / Vanilla JavaScript
* [Tailwind CSS](https://tailwindcss.com/)
* [Monaco Editor](https://microsoft.github.io/monaco-editor/)
* [Marked.js](https://marked.js.org/)
* SheetJS (XLSX) & Mammoth.js (DOCX)
