# -awesome-list-explorer
Smart Awesome List Explorer 🚀 | A zero-dependency, single-file web app that transforms Markdown files &amp; GitHub READMEs into an interactive, searchable resource dashboard with native mobile UX &amp; Arabic RTL support.


<div align="center">

# 🚀 Awesome List Explorer

**Transform Markdown files and GitHub repositories into an interactive, organized, and instantly searchable resource dashboard!**

[![HTML5](https://img.shields.io/badge/HTML5-Single_File-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)
[![Vanilla JS](https://img.shields.io/badge/Vanilla_JS-Zero_Dependencies-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#)
[![UI/UX](https://img.shields.io/badge/Design-60%2F30%2F10_Architecture-FFAA5C?style=for-the-badge)](#)
[![RTL & LTR](https://img.shields.io/badge/Support-RTL_%26_LTR-2DD4BF?style=for-the-badge)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

</div>

---

## 💡 Overview

**Awesome List Explorer** is a full-featured web application built entirely within a **Single-File Architecture (`index.html`)** with **Zero Dependencies**. It is specifically engineered to solve the challenge of navigating massive Markdown files and popular GitHub `Awesome Lists`. By parsing raw Markdown on the fly, it transforms long text documents into an intuitive dashboard featuring collapsible categories, smart resource cards, and instant filtering.

Designed with a strict **60/30/10 color architecture** and **WCAG AAA contrast compliance**, the application delivers a sleek desktop dashboard experience alongside a **Native Mobile App UX** complete with a bottom navigation bar and smooth slide-over bottom sheets.

---

## ✨ Key Features

### 🎨 1. Modern UI/UX & Native Mobile Experience
* **Native Mobile-App Feel:** Equipped with a fixed bottom navigation bar and smooth slide-over bottom sheets for browsing categories, importing files, and adjusting settings effortlessly with one hand.
* **Desktop Dashboard Layout:** Features a sticky hierarchical Table of Contents (TOC) sidebar with automatic **ScrollSpy** tracking as you scroll through sections.
* **Adaptive Dark & Light Modes:** Seamless theme switching engineered with CSS Design Tokens, automatically persisted in `localStorage`.
* **Flexible Layouts (Grid & List Views):** Toggle instantly between a responsive multi-column card grid and a compact list view.

### 🔍 2. Smart Search Engine & Multilingual Normalization
* **Debounced Live Search:** Filter thousands of resources in real time without UI lag or frame drops.
* **Live Keyword Highlighting:** Automatically highlights matching search terms inside card titles and descriptions while dynamically updating category item counters.
* **Arabic & Multilingual Normalization:** Built-in text normalization that unifies character variations and ignores diacritics for accurate bilingual searching.
* **Keyboard Shortcuts:** Press `/` or `Ctrl + K` (`Cmd + K` on Mac) anywhere to focus the search bar immediately.

### 🔗 3. Direct GitHub Integration & Nested Navigation
* **GitHub API Fetching:** Enter any repository shorthand (e.g., `sindresorhus/awesome` or `vinta/awesome-python`) or paste a full GitHub URL to fetch, decode, and render its `README.md` directly.
* **Nested Repository Exploration:** Clicking a card that points to another GitHub repository opens it directly inside the explorer, maintaining a full **Navigation Stack**, interactive **Breadcrumbs**, and a **Back** button.
* **Session Recovery:** Automatically caches your last uploaded local file in `sessionStorage` so you can restore your workspace with a single click.

### 🛡️ 4. Security, Privacy & Performance
* **100% Client-Side Privacy:** Local `.md` files are read directly in your browser using the File API—nothing is ever uploaded to an external server.
* **XSS Protection & URL Sanitization:** Strict HTML escaping and protocol validation (`http:`, `https:`, `#`) while safely rendering inline Markdown (`code`, **bold**, *italic*, ~~strikethrough~~) and secondary link chips.
* **High-Efficiency DOM Rendering:** Powered by `DocumentFragment` batching, `IntersectionObserver`, and `AbortController` to prevent memory leaks and cancel redundant network requests.

---

## 🛠️ Quick Start & Usage

No build tools, `npm` packages, or local servers are required:

1. **Clone or Download:**
   ```bash
   git clone https://github.com/AminOqbah/awesome-list-explorer.git
   ```
2. **Run:**
   Open `index.html` (or `awesomelist.html`) directly in any modern web browser on desktop or mobile.
3. **Explore Resources:**
   * 📂 **Local File:** Click **"Upload File"** and select any `.md`, `.markdown`, or `.txt` file from your device.
   * 🌐 **GitHub Repository:** Type a repository name (e.g., `avelino/awesome-go`) in the GitHub input field and click **"Open Repo"**.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| `/` or `Ctrl + K` | Focus the search input immediately |
| `Tab` / `Shift + Tab` | Navigate through interactive resource cards |
| `Enter` / `Space` | Open the focused resource card or GitHub repository |

---

## 🏗️ Internal Architecture

Although packaged as a single `.html` file for maximum portability, the codebase follows strict modular software engineering principles:

1. **Design Tokens (CSS Variables):** Complete `60/30/10` color palette tokens for Dark and Light themes, spacing scales, and elevation shadows.
2. **Centralized `AppState`:** Single source of truth managing theme preferences, view modes, navigation stack, and parsed data.
3. **Security & Text Utilities:** HTML sanitization, safe inline Markdown rendering, URL resolution, and text normalization.
4. **Resilient Markdown Parser:** Regex-driven state machine capable of extracting headings (`h1`–`h6`), nested lists, primary links, descriptions, and extra link chips while ignoring code blocks.
5. **Batched DOM Renderer & ScrollSpy:** High-speed DOM construction using `DocumentFragment` paired with an `IntersectionObserver` for active section tracking.

---

## 🌐 Deployment (GitHub Pages)

To host this app live for free on **GitHub Pages**:
1. Rename `awesomelist.html` to `index.html` in the root of your repository.
2. Go to your repository **Settings** → **Pages**.
3. Under **Build and deployment**, select **Deploy from a branch** and choose the `main` branch (`/root`).
4. Click **Save**—your live web app will be ready within seconds!

---

## 🤝 Contributing & License

Contributions, issues, and feature requests are welcome!  
This project is open-source and available under the **[MIT License](LICENSE)**.
