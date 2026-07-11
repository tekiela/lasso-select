# Turtlestitch Lasso Selection Tool

An intuitive rectangle lasso multi-selection tool: Alt-click toggle selection, Select-All shortcut, and Delete explicitly built for the Turtlestitch editor!

This tool works flawlessly on the official editor at **`https://turtlestitch.org`** (and supports legacy Snap! 11 installs).

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
## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Cmd+A` / `Ctrl+A` | Select all blocks and comments in the workspace |
| `Backspace` / `Delete` | Delete the active selection |
| `Alt` + Click | Toggle a block or comment in/out of the selection |

