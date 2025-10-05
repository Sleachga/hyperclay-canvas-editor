# Hyperclay Canvas Editor

An Illustrator-style canvas editor built as a single-file HTML application using the Hyperclay platform.

## Features

### Drawing Tools

- **Selection Tool** (V) - Move, resize, and rotate objects
- **Rectangle Tool** (M) - Draw rectangles and squares
- **Ellipse Tool** (L) - Draw ellipses and circles

### Canvas Controls

- **Pan**: Hold spacebar and drag
- **Zoom**: Mouse wheel (Cmd/Ctrl + wheel for finer control)
- **Infinite canvas workspace**

### Object Manipulation

- **Move**: Drag selected objects
- **Resize**: Drag corner/edge handles
- **Rotate**: Drag rotation handle (circular icon above selection)
- **Shift+Resize**: Maintain aspect ratio (proportional scaling)
- **Shift+Draw**: Create perfect squares/circles
- **Delete**: Press Delete or Backspace key

### Panels

- **Properties Panel**: Adjust fill color, stroke color, and stroke width
- **Layers Panel**: View all objects, drag to reorder (z-index), double-click names to rename

### Persistence

- Auto-saves changes using Hyperclay platform
- Selection state persists across page reloads
- All changes stored directly in the DOM

## Technology

- Single-file HTML architecture
- SVG for canvas rendering
- jQuery for DOM manipulation
- [Hyperclay](https://hyperclay.com) for automatic persistence
- No build process required

## Development

See [Hyperclay docs](https://docs.hyperclay.com/docs/docs-tldr-paste-in-llm/) for more info

See [backlog.md](backlog.md) for planned features and development roadmap.
