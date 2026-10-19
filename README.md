# BrowserForge 🔨

BrowserForge is a zero-setup AI IDE and Native Web Agent that runs in your browser. It allows you to mount a local workspace, edit code, view documents, and leverage various flagship AI models to autonomously perform file operations right on your machine.

## ✨ Features
* **Zero Backend:** No server component — the UI runs in your browser. UI libraries (Monaco, Tailwind, SheetJS, Mammoth, marked) are loaded from CDNs, so an internet connection is required. Your workspace files stay local.
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

## 🛠️ Tech Stack
* HTML5 / Vanilla JavaScript
* [Tailwind CSS](https://tailwindcss.com/)
* [Monaco Editor](https://microsoft.github.io/monaco-editor/)
* [Marked.js](https://marked.js.org/)
* SheetJS (XLSX) & Mammoth.js (DOCX)
