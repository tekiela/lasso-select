# TurtleStitch Lasso Select

Tired of deleting 50 blocks one by one? This new feature for TurtleStitch lets you lasso-select, move, and delete groups of blocks right in the editor.

This tool also works directly on **[TurtleStitch](https://turtlestitch.org)** because its browser based.

![Lasso Selection Banner](https://img.shields.io/badge/Snap!-Lasso%20Selection-brightgreen?style=for-the-badge&logo=javascript)
![Version](https://img.shields.io/badge/version-3.0-blue?style=for-the-badge)

---

## ✨ Features
* **Lasso SELECTION:** Click and drag to draw a bright green bounding box to select blocks.
* **Lasso GROUP:** Lassoing a group of blocks selects the entire connected group.
* **INVERT w. Alt-Drag:** Hold `Alt` while dragging a lasso to instantly invert block selection!
* **ADD w. Alt-Click:** Press and hold `Alt` (or `Option` on macOS) to add to, or remove it from, the active selection. Clicking mid-group toggles the group status.
* **Select ALL:** Press `Cmd+A` (macOS) or `Ctrl+A` (Windows/Linux) to select all blocks in the workspace.
* **Deletion:** Press `Backspace` or `Delete` keys to delete selected blocks.
* **Right-Click:** selected group to see context menu and duplicate or delete the selection.

---

## 🚀 Installation

### Method 1: TurtleStitch Library (Recommended for Safari & Firefox)
This runs 100% offline, and works across all browsers BUT demands JavaScript extensions ON:
1. **Right-click** and save this link: [lasso_selection.xml](https://raw.githubusercontent.com/tekiela/snap11-lassoselect/main/libraries/lasso_selection.xml).
2. Open any TurtleStitch window.
3. Open the **Settings** menu (gear icon) and make sure **Enable JavaScript extensions** is **checked**.
4. Drag and drop the `lasso_selection.xml` file into the editor (or via **File -> Import...**).
5. Find the new block **`[enable lasso selection]`** under the **Control** category palette and click it once.

---

### Method 2: Bookmarklet (Zero-Install)
Bookmarklets run JavaScript directly in your active tab and can be run online AND offline.

#### AUTOMATIC UPDATE — CDN Loader *(always up to date, requires internet)*
1. Create a new bookmark in your browser named **TurtleStitch Lasso**.
2. Replace the URL with this code:
   ```javascript
   javascript:(function(){var targetWin=window;try{for(var i=0;i<window.frames.length;i++){if(window.frames[i].ScriptsMorph){targetWin=window.frames[i];break;}}}catch(e){}var s=targetWin.document.createElement('script');s.src='https://cdn.jsdelivr.net/gh/tekiela/snap11-lassoselect@main/extensions/lasso_selection/inject.js';targetWin.document.body.appendChild(s);})();

3. Open the editor and click the browser-bookmark to activate (confirmation will appear at bottom when loaded correctly)

#### MANUAL UPDATE — offline bookmarklet *(no internet needed)*
Download the offline version here: [minified_bookmarklet.txt](minified_bookmarklet.txt).
1. Open 'minified_bookmarklet.txt' — you will see one long line of text.
2. Select all and copy it.
3. Create a new bookmark named **Snap! Lasso v3 (offline)** and paste it into the URL field.
4. Open a Snap! editor page and click the bookmark to activate.

---

### Method 3: Browser Extension (Persistent w. restart)
Loads the lasso tool automatically on every Snap! tab you open.

#### For Chrome / Chromium Browsers:
1. Download or clone this repository to your computer.
2. Open Chrome and navigate to `chrome://extensions/`.
3. Enable **Developer mode** (top-right toggle).
4. Click **Load unpacked** (top-left) and select the `extensions/lasso_selection` directory.

#### For Firefox:
1. Open Firefox and go to `about:debugging`.
2. Click **This Firefox** -> **Load Temporary Add-on...**
3. Select `manifest.json` inside the `extensions/lasso_selection` folder.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Cmd+A` / `Ctrl+A` | Select all blocks and comments in the workspace |
| `Backspace` / `Delete` | Delete the active selection |
| `Alt` + Click | Toggle a block or comment in/out of the selection |

