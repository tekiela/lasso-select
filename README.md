# Lasso Select

Tired of deleting 50 blocks one by one? This new feature for **Snap!** and **TurtleStitch** lets you lasso-select, move, duplicate, and delete groups of blocks right in the editor.

![Lasso select demo](assets/start_small.gif)

It works on both in local installs and online because it's completely browser-based.

![Lasso Selection Banner](https://img.shields.io/badge/Snap!-Lasso%20Select-brightgreen?style=for-the-badge&logo=javascript)
![Version](https://img.shields.io/badge/version-3.1-blue?style=for-the-badge)

---

## ✨ Features
* **Lasso SELECT:** Click and drag to draw an orange bounding box to select blocks.
* **MULTI SELECT  w. Alt-Click:** Press and hold `Alt` (or `Option`) to add to, or remove it from, the active selection. Clicking mid-group toggles the group status.
* **INVERT w. Alt-Drag:** Hold `Alt` while dragging a lasso to instantly invert block selection!
* **Select ALL:** Press `Cmd+A` (mac) or `Ctrl+A` (Win) to select all blocks in the workspace.
* **Deletion:** Press `Backspace` or `Delete` keys to delete selected blocks.
* **Right-Click:** selected group to see context menu and duplicate or delete the selection.

---

## 🚀 Installation


### Method 1: Firefox addon - One click to install
https://addons.mozilla.org/en-US/firefox/addon/lasso-select-turtlestitch-snap/

### Method 2: Bookmarklet (Zero-Install)
This runs 100% offline, and works across all browsers BUT demands JavaScript extensions ON:
1. **Right-click** and save this link: [lasso-select.xml](https://raw.githubusercontent.com/tekiela/lasso-select/main/libraries/lasso-select.xml).
2. Open any TurtleStitch window.
3. Open the **Settings** menu (gear icon) and make sure **Enable JavaScript extensions** is **checked**.
4. Drag and drop the `lasso-select.xml` file into the editor (or via **File -> Import...**).
5. Find the new block **`[enable lasso-select]`** under the **Control** category palette and click it once.

---

### Method 3: Bookmarklet (Zero-Install)
Bookmarklets run JavaScript directly in your active tab and can be run online AND offline.

**3A AUTOMATIC UPDATE** — Online Bookmarklet *(always up to date, requires internet)*
1. Create a new bookmark in your browser named **Lasso Select**.
2. Replace the URL with this code:
   ```javascript
   javascript:(function(){var targetWin=window;try{for(var i=0;i<window.frames.length;i++){if(window.frames[i].ScriptsMorph){targetWin=window.frames[i];break;}}}catch(e){}var s=targetWin.document.createElement('script');s.src='https://cdn.jsdelivr.net/gh/tekiela/lasso-select@main/extensions/lasso-select/inject.js';targetWin.document.body.appendChild(s);})();
   ```
3. Open the editor and click the browser-bookmark to activate (confirmation will appear at bottom when loaded correctly).

**3B MANUAL UPDATE** — Offline Bookmarklet *(no internet needed)*
Download the fully offline version here: [offline-bookmarklet.txt](https://raw.githubusercontent.com/tekiela/lasso-select/main/offline-bookmarklet.txt).
1. Open 'offline-bookmarklet.txt' — you will see one massive block of code.
2. Select all and copy it.
3. Create a new bookmark named **Lasso Select** and paste the massive block of code into the URL field.
4. Open a Snap! editor page and click the bookmark to activate.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Cmd+A` / `Ctrl+A` | Select all blocks and comments in the workspace |
| `Backspace` / `Delete` | Delete the active selection |
| `Alt` + Click | Toggle a block or comment in/out of the selection |

---

## 🐧 Linux Users (Alt-Key Troubleshooting)

In many Linux desktop environments (like GNOME/Ubuntu), holding the `Alt` key and dragging the mouse is a system-level shortcut used to move application windows. This will prevent the extension's **Alt-Drag** and **Alt-Click** features from working in your browser.

To fix this, you can free up the `Alt` key by changing the window-move modifier to the `Super` (Windows) key. Just run this two-liner in your terminal:

```bash
# Free up the Alt key for browser applications
gsettings set org.gnome.desktop.wm.preferences mouse-button-modifier "<Super>"
```

