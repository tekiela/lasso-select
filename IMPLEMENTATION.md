# Lasso Select Architecture: TurtleStitch and Snap!

This note documents the specific patches used to integrate Lasso Select into `morphic.js` and `widgets.js`.

## 🏗️ New Classes
- **`LassoGroupMorph` (inherits `Morph`)**: Acts as a transparent container for grouped blocks. Overrides `topMorphAt` to pass empty-space clicks through to the background.

## 🪝 Patched Methods
- **`ScriptsMorph.mouseDownLeft`**: Spawns the transparent lasso `BoxMorph` and calls `lockMouseFocus`.
- **`ScriptsMorph.mouseMove`**: Resizes the lasso bounding box during the drag.
- **`ScriptsMorph.mouseClickLeft`**: Calculates intersection using `fullBounds()` and groups the blocks.
- **`HandMorph.processMouseDown`**: Intercepts `Alt/Option` clicks to toggle blocks in/out of groups.
- **`HandMorph.processMouseUp`**: Manually forces the `mouseClickLeft` callback if a lasso drag ends over a child block (preventing ghost lasso artifacts).
- **`ScriptsMorph.toXML`**: Calls `.unpack()` on all active lasso groups before serialization to ensure standard XML output.
- **`Morph.rootForGrab` & `Morph.contextMenu`**: Modified to bubble up to the `LassoGroupMorph` if a block is currently selected.

## 🔒 Engine Safety
- **Identification:** Group identification relies exclusively on prototype fingerprinting (`isLassoGroup = true`) rather than `constructor.name` to survive minification and live-reloads.
- **Bookmarklet Wrapper:** The bookmarklet contains an iframe-traversing wrapper (`window.frames`) to ensure the payload is injected into the correct window context for TurtleStitch (which nests Snap! inside an iframe), while remaining fully compatible with top-level standalone environments.

## 🎨 Visual Customizations
- **Color Profile:** Enforces a customized, darker/less saturated orange (`Color(225, 130, 25)`) for both the lasso bounding box and the block highlight glows.
- **TurtleStitch Hard-Edge Fix:** Due to TurtleStitch's flat-design configurations (`MorphicPreferences.isFlat`), `addHighlight()` natively generates a flat, hard-edged outline rather than a fuzzy neon shadow. The extension injects `aMorph.activeBorder = 3` prior to triggering the highlight to forcefully tighten the thickness of this edge, preventing it from appearing overly loud or thick.
