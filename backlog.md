# Canvas Editor - Feature Backlog

## Core Canvas Features
- [x] Canvas initialization and rendering
- [x] Pan and zoom controls (mouse wheel, drag with spacebar)
- [ ] Grid system with snap-to-grid toggle
- [ ] Rulers (horizontal/vertical)
- [x] Infinite canvas workspace
- [ ] Zoom percentage display
- [ ] Fit to view / Zoom to selection
- [ ] Reset view button
- [ ] Mini-map/navigator panel
- [x] Canvas dirty flag (only redraw when needed) - Using MutationObserver
- [ ] Object culling (don't render off-screen objects)

## Drawing Tools
- [x] Selection tool (move, resize, rotate objects)
- [x] Rectangle tool
- [x] Circle/Ellipse tool
- [ ] Line tool
- [ ] Pen tool (bezier curves)
- [ ] Freehand/Pencil tool
- [ ] Text tool

## Object Manipulation
- [ ] Multi-select (shift-click, drag marquee selection box)
- [x] Bounding box visual feedback
- [x] Selected object highlighting
- [x] Object layering (drag to reorder in layers panel)
- [ ] Group/ungroup objects
- [ ] Align objects (left, center, right, top, middle, bottom)
- [ ] Distribute objects evenly
- [ ] Duplicate objects (Cmd+C/Cmd+V)
- [ ] Duplicate in place (Cmd+D)
- [x] Delete objects (Delete/Backspace)
- [x] Transform handles (resize, rotate)
- [ ] Snap guides when aligning objects
- [ ] Smart guides (distance from other objects)
- [ ] Nudge with arrow keys
- [ ] Lock/unlock objects
- [ ] Hide/show objects
- [x] Object naming (for layers panel) - Double-click to edit
- [ ] Z-index visual indicator
- [x] Precise input fields (X, Y, W, H, Rotation)

## Styling
- [x] Fill color picker (with hex input)
- [x] Stroke color picker
- [x] No fill / No stroke options (set stroke width to 0)
- [x] Stroke width control (defaults to 0 when empty)
- [ ] Opacity/transparency slider
- [ ] Stroke style (solid, dashed, dotted)
- [ ] Corner radius for rectangles
- [ ] Recent colors palette
- [ ] Color presets/swatches
- [ ] Eyedropper tool

## Text Editing
- [ ] Font family selection
- [ ] Font size control
- [ ] Bold, italic, underline
- [ ] Text alignment (left, center, right)
- [ ] Text color

## History & State (Hyperclay Pattern)
- [x] Store canvas state directly in DOM (SVG elements)
- [x] Hyperclay auto-persistence using `persist=""` attribute on inputs
- [x] Call `hyperclay.savePage()` on web, fetch('/save/index') on localhost
- [x] Auto-save after shape changes (drag, resize, rotate, color changes)
- [x] Restore selection state on page load
- [x] Clear layers panel before save (regenerated on load)
- [x] Clear highlight layer before save (regenerated on interaction)
- [ ] Undo/Redo (Cmd+Z, Cmd+Shift+Z)
- [x] Handle missing state gracefully (initialize empty canvas)
- [ ] Optimize for many objects (100+ shapes)

## Export/Import
- [ ] Export as SVG
- [ ] Export as PNG
- [ ] Export as JSON (for reimport)
- [ ] Export canvas code (HTML/CSS/JS to recreate canvas)
- [ ] Export canvas code (framework-specific: React, Vue, etc.)
- [ ] Copy code to clipboard
- [ ] Import SVG
- [ ] Import JSON

## UI/UX (Illustrator-style - Modern & Simple)
- [x] Dark theme (#2b2b2b background, #1e1e1e panels)
- [x] Top menu bar (static, no dropdowns yet):
  - [ ] File menu (New, Save, Export as SVG, Export as PNG, Export Code)
  - [ ] Edit menu (Undo, Redo, Cut, Copy, Paste, Duplicate, Select All)
  - [ ] Object menu (Group, Ungroup, Lock, Unlock, Show, Hide)
  - [ ] Arrange menu (Bring to Front, Bring Forward, Send Backward, Send to Back)
  - [ ] View menu (Zoom In/Out, Fit to View, 100%, Show/Hide Grid, Rulers, Guides)
  - [ ] Help menu (Keyboard Shortcuts reference)
- [x] Menu bar styling (~32px height, dark background)
- [x] Right vertical toolbar with SVG icons:
  - [x] Selection tool icon (arrow/pointer)
  - [x] Rectangle tool icon
  - [x] Circle tool icon
  - [ ] Line tool icon
  - [ ] Pen tool icon
  - [ ] Pencil tool icon
  - [ ] Text tool icon
  - [ ] Eyedropper tool icon
  - [ ] Hand/Pan tool icon
  - [ ] Zoom tool icon
- [x] Toolbar styling (2-column grid, 44px buttons)
- [x] Top properties bar (X, Y, W, H, Rotation inputs)
- [x] Left sidebar panels (240px):
  - [x] Layers panel (with drag-to-reorder, double-click to rename)
  - [x] Properties/Appearance panel (fill, stroke, stroke width)
  - [ ] Color swatches panel
- [x] Flat monochrome icons (light gray #e0e0e0)
- [x] Active tool: bright accent color (#1473e6 blue)
- [x] Clean system fonts (-apple-system, sans-serif)
- [x] Subtle 1px borders (#3a3a3a)
- [x] White canvas area (#ffffff) - high contrast
- [x] Smooth hover states (opacity/background transitions)
- [ ] Icon tooltips on hover (show tool name + shortcut)
- [ ] Context menu (right-click)
- [x] Hover states and visual feedback (hover highlights on shapes)

## Keyboard Shortcuts (Illustrator-style)
### Tools
- [x] V - Selection tool
- [x] M - Rectangle tool
- [x] L - Ellipse/Circle tool
- [ ] \ - Line tool
- [ ] P - Pen tool
- [ ] N - Pencil tool
- [ ] T - Text tool
- [ ] I - Eyedropper tool
- [ ] H - Hand/Pan tool
- [ ] Z - Zoom tool

### Edit
- [ ] Cmd/Ctrl + Z - Undo
- [ ] Cmd/Ctrl + Shift + Z - Redo
- [ ] Cmd/Ctrl + C - Copy
- [ ] Cmd/Ctrl + V - Paste
- [ ] Cmd/Ctrl + D - Duplicate
- [ ] Cmd/Ctrl + X - Cut
- [ ] Cmd/Ctrl + A - Select All
- [x] Delete/Backspace - Delete selected
- [ ] Cmd/Ctrl + G - Group
- [ ] Cmd/Ctrl + Shift + G - Ungroup

### Arrange
- [ ] Cmd/Ctrl + ] - Bring Forward
- [ ] Cmd/Ctrl + [ - Send Backward
- [ ] Cmd/Ctrl + Shift + ] - Bring to Front
- [ ] Cmd/Ctrl + Shift + [ - Send to Back

### View
- [ ] Cmd/Ctrl + 0 - Fit to view
- [ ] Cmd/Ctrl + 1 - 100% zoom
- [x] Cmd/Ctrl + wheel - Zoom in/out
- [ ] Cmd/Ctrl + + - Zoom in
- [ ] Cmd/Ctrl + - - Zoom out
- [ ] Cmd/Ctrl + ' - Show/hide grid
- [ ] Cmd/Ctrl + ; - Show/hide guides
- [ ] Cmd/Ctrl + R - Show/hide rulers

### Object Manipulation
- [ ] Arrow keys - Nudge 1px
- [ ] Shift + Arrow keys - Nudge 10px
- [x] Shift + resize - Constrain proportions (maintain aspect ratio)
- [x] Shift + draw - Create squares/circles (constrain to 1:1)
- [ ] Alt/Option + drag - Duplicate while dragging
- [ ] Cmd/Ctrl + 2 - Lock selection
- [ ] Cmd/Ctrl + Alt + 2 - Unlock all

### Other
- [ ] Cmd/Ctrl + S - Save (triggers Hyperclay save)
- [x] Spacebar (hold) - Pan canvas
- [ ] Cmd/Ctrl (hold) - Temporarily switch to Selection tool

## Edit/View Modes
- [ ] Edit mode: Full editing capabilities
- [ ] View mode: Pan/zoom only, read-only display
- [ ] Mode toggle button

## Advanced Features (Future)
- [ ] Custom shapes library
- [ ] Image upload and placement
- [ ] Path editing (bezier curve manipulation)
- [ ] Boolean operations (union, subtract, intersect, exclude)
  - Note: Use paper.js for implementation - has built-in `path1.unite()`, `path1.subtract()`, etc.
  - Handles complex intersections, bezier curves, and edge cases
  - ~100KB dependency but battle-tested
- [ ] Clipping masks
- [ ] Gradients
- [ ] Shadows and effects
- [ ] Artboards/multiple canvases

## Collaboration & Sharing (Future)
- [ ] View-only mode link generation
- [ ] Embed code
- [ ] Template gallery
- [ ] Multi-user editing (if needed)
