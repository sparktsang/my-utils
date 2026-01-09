# 🛠️ Personal Utility Toolkit

A lightweight, single-page web application hosted on GitHub Pages. This toolkit replaces the need to open heavy IDEs (like Spyder/VS Code) or risk privacy by using ad-ridden online converters. It performs text processing tasks instantly within the browser.

**👉 [Click here to use the App](https://sparktsang.github.io/my-utils/)**  

---

## 🧰 Current Tools

### 1. URL to Readable Format
Decodes messy, percent-encoded URLs into clean, human-readable Unicode strings.
- **Input:** `https://example.com/%E4%BD%A0%E5%A5%BD`
- **Output:** `https://example.com/你好`
- **Use Case:** Perfect for cleaning up links before sharing or documenting.

### 2. Smart Markdown TOC Generator
Automatically generates a Table of Contents for Markdown files based on `###` headers.
- **Smart Filtering:** It intelligently detects if a "Contents" section already exists and ignores it, preventing recursive duplication.
- **Auto-Formatting:** Automatically prepends `### Contents` with correct line spacing.
- **Logic:** Handles Chinese/Unicode characters and complex symbols perfectly when generating anchor links (slugs).

### 3. AI Studio JSON Converter (New!)
A specialized tool for extracting conversation history from **Google AI Studio** export files.
- **The Problem:** AI Studio exports are complex JSON files mixed with internal "thought processes" and metadata. They are unreadable to humans, and surprisingly, **no existing online tool** handles this conversion simply.
- **The Solution:** Just **drag and drop** the raw JSON file (even without a file extension). The app instantly parses the structure, filters out hidden internal thoughts (`isThought: true`), and outputs a clean, readable Markdown conversation log.
- **Logic:** Implements the exact extraction logic used in Python data pipelines but runs instantly in your browser.

---

## 🚀 Why Build This? (The Philosophy)

There are thousands of "free online tools" out there, so why build another one?

### 1. 🔒 100% Privacy & Security
Most online converters process data on their servers or are loaded with tracking scripts. This app runs **entirely in your browser (Client-Side JavaScript)**. No data is ever sent to a server. It is safe to use with sensitive work documents or internal links.

### 2. ⚡ Zero Latency & Zero Setup
- **Faster than Python:** No need to launch Anaconda, Spyder, or run a `.py` script. The browser's V8 engine parses text instantly.
- **Access Anywhere:** Works on mobile, tablets, or any computer without a development environment.

### 3. 🎯 Tailor-Made Logic
Generic tools (like VS Code plugins) use generic logic. This app is customized for a specific workflow. For example, the TOC generator specifically filters out old directories and formats spacing exactly how I want it. **It adapts to the user, not the other way around.**

---

## 🤝 Fork & Extend

This repository is designed to be a template. The architecture is intentionally simple (single `index.html` with vanilla JS/CSS).

**I highly encourage you to fork this repository and make it your own!**

### How to add your own tool:
1. **Fork** this repo.
2. Edit `index.html`.
3. Add a new `<button>` in the sidebar.
4. Copy/Paste a `.tool-section` div and customize the inputs.
5. Add your JavaScript function at the bottom.
6. Enable **GitHub Pages** in your settings.

Build the tools that solve **your** specific problems. Happy coding!
