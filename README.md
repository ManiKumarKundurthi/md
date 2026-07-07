# Markdown Editor & Viewer

A minimal, high-performance, responsive Markdown editor and real-time previewer styled with a custom **Material Design 3 (Dark Blue, Pure Black, and Pure White)** color palette. Designed for fast editing, syntax highlighting, and clean mathematics rendering.

Live Demo: [manikumarkundurthi.github.io/md](https://manikumarkundurthi.github.io/md)

---

## Features

*   **Real-time Side-by-Side Preview:** See your formatted Markdown render instantly as you type, with synchronized vertical scrolling.
*   **Material Design 3 Themes:** Cycle seamlessly through three tailored themes (with automatic adaptation of code block contrasts):
    *  **Dark Blue:** Default elegant M3 dark theme.
    *  **Pure Black:** True-black background optimization for OLED screens.
    *  **Pure White:** A clean, high-contrast light mode.
*   **LaTeX Mathematical Equations:** Built-in support for rendering inline math using `$e = mc^2$` and block math using `$$ ... $$` via the high-performance **KaTeX** engine.
*   **Code Syntax Highlighting:** Automatic detection and beautiful language styling for code snippets powered by **Highlight.js**.
*   **Robust Security:** Deep client-side XSS (Cross-Site Scripting) protection via **DOMPurify** sanitization.
*   **Distraction-Free Mode:** Easily collapse or expand the Editor or Preview panes independently using header controls.
*   **Local Auto-Save:** Automatically saves your work to your browser's local storage as you type, keeping your draft safe even if you reload.
*   **One-Click Exports:** Quick-action buttons to instantly download your document as a raw `.md` file or a fully styled standalone `.html` web page.

---

## Architecture & Technologies Used

This application is built entirely as a single-page utility with zero heavy framework dependencies, keeping load times near-instantaneous:

*   **Tailwind CSS (v3 CDN):** Used for fluid layouts, flex positioning, and Material 3 design token layouts.
*   **Marked.js (v5+):** A lightning-fast Markdown parser and compiler.
*   **DOMPurify:** Secures the parsed HTML payload before injecting it into the Document Object Model.
*   **KaTeX:** High-speed math typesetting library used to handle complex formulas cleanly.
*   **Highlight.js:** Handles local context formatting inside dynamic code blocks.

---

## Project Structure

```text
├── index.html        # Main application file (UI structure, CSS tokens, and core JS logic)
└── README.md         # Documentation

```

---

## Local Setup & Development

Because this application relies strictly on client-side JavaScript libraries loaded via secure CDNs, you do not need to install `npm`, `node`, or run a complex local server bundle.

1. Clone or download this repository:
```bash
git clone [https://github.com/manikumarkundurthi/md.git](https://github.com/manikumarkundurthi/md.git)
cd md

```


2. Simply double-click the `index.html` file to launch it locally in any modern desktop or mobile browser.
3. *Alternative:* If you prefer a local development environment to test layout adjustments without caching, serve it using python:
```bash
python3 -m http.server 8000

```


Then navigate to `http://localhost:8000` in your web browser.

---

## Deploying to GitHub Pages

To update or re-host this tool yourself under your primary GitHub Pages path:

1. Push your `index.html` to the root directory of your public repository named `md`.
2. Navigate to your repository's **Settings** tab on GitHub.
3. Choose **Pages** from the left-hand navigation sidebar.
4. Set the deployment source branch to **`main`** (or `master`) and folder path to **`/ (root)`**.
5. Hit **Save**. The page will generate automatically within a few moments at your public directory.

---

## License

This project is open-source and free to use. Feel free to modify, expand, or self-host as needed!

```
