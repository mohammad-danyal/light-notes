# Stateless Vault

A self-contained, privacy-first, in-memory note-taking environment.

## 🛡️ Design Philosophy

Stateless Vault is built on the principle of **absolute user control**. Unlike traditional note-taking apps that automatically sync to the cloud or store data in hidden browser databases (IndexedDB/LocalStorage), this vault exists **only in your computer's RAM** while the tab is open.

- **Zero Persistence**: No data is ever written to your disk by the browser.
- **Privacy by Default**: Closing the tab results in total data destruction.
- **Explicit Save**: You are the sole owner of your data. The only way to "save" is to explicitly export your vault as a ZIP file.

## ✨ Features

- **Block-Based Editing**: Use Slash commands (`/`) to insert headings, lists, code blocks, and dividers.
- **Folder Hierarchy**: Organize notes into nested folders with drag-and-drop support.
- **Stateless Sessions**: Clearly marked session status with a dedicated "In-Memory" safety notice box in the sidebar.
- **Deterministic Portability**: Export your entire vault as a ZIP containing an `index.json` (metadata) and individual `.md` files (content).
- **Quick Finder**: Lightning-fast search across all in-memory notes (`Ctrl/Cmd + K`).
- **Dark Mode**: A beautiful, minimalist interface that respects your system preferences.
- **Safety Mechanism**: Prevents accidental data loss by prompting you before you refresh or close the tab if changes have been made.

## 🚀 How to Use

### 1. Starting a Session
Simply open the HTML file in any modern browser. You start with a clean slate and a "Welcome" note in your drafts.

### 2. Creating Content
- **New Note/Folder**: Use the icons at the top of the sidebar.
- **Slash Menu**: Type `/` in any empty block to transform it.
- **Organize**: Drag and drop notes or folders to rearrange your vault hierarchy.

### 3. Saving Your Work (Crucial)
Since this app is stateless, **refreshing the page or closing the tab will delete your current work**.
- Click the **Export ZIP to save →** notice in the sidebar, or go to **Settings** (Gear icon) → **Export ZIP**.
- This downloads a portable backup of your entire session.

### 4. Restoring a Session
- Go to **Settings** → **Import ZIP**.
- Select a previously exported ZIP file to restore your notes and folder structure into the current session's memory.

## 🛠️ Technical Stack

- **Pure HTML/JS**: No build steps, zero-install, single-file distribution.
- **Tailwind CSS**: For a modern, responsive, and accessible UI.
- **fflate**: High-performance, in-memory ZIP compression and decompression.
- **Stateless Core**: A custom-built state engine managing the in-memory graph of notes and folders.

---
*Made by Danyal*