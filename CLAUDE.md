# Hyperclay Platform Documentation

## Overview

Hyperclay is a platform for creating single-file HTML applications where the HTML serves as both the frontend and the database. The platform automatically handles persistence and provides edit/view modes.

## Key Concepts

### Single-File Applications
- HTML serves as both UI and database
- All state stored in the DOM
- Automatic persistence to backend
- No separate server/database needed

### Save Lifecycle
Changes are saved when:
- DOM mutations occur
- Clicking buttons with `trigger-save` class
- Using `CMD/Ctrl+S` keyboard shortcut

### Edit vs View Modes
- Edit mode: Interactive, can modify content
- View mode: Read-only display
- `editmode` attribute added to `<html>` element
- Control visibility with `option:` attributes

## Hyperclay Starter Kit

**Location**: `/js/hyperclay-starter-kit.js` (available when hosted on Hyperclay)

The Starter Kit provides:
- Automatic DOM saving utilities
- View/edit mode support
- Custom event attributes
- File upload helpers

## Custom Attributes

### Event Attributes
- `onrender`: Execute code when element renders
- `onbeforesave`: Clean up before saving (remove admin UI, etc.)
- `onclickaway`: Trigger when clicking outside element
- `onpagemutation`: React to DOM changes

### Visibility Control
Use `option:` attributes for conditional rendering based on any HTML attribute.

## Development Approach

### Recommended Workflow
1. **Start with jQuery** for DOM manipulation
2. **Build with basic DOM operations** first
3. **Add Starter Kit utilities** as needed
4. **Let Hyperclay handle persistence** automatically

### jQuery-First Philosophy
- Use jQuery for DOM changes
- Hyperclay automatically detects modifications
- Changes persist without manual save logic

## Advanced Features

### Multi-Tenant Support
Enable signups to transform your app into a multi-user platform

### Tailwind CSS Integration
Include these for Tailwind support:
- `/css/tailwind-base.css`
- `/js/vendor/tailwind-play.js`

### File Operations
- `hyperclay.uploadFile()`: Upload files
- `hyperclay.sendMessage()`: Send messages from anonymous users

## Best Practices

### DOM as Component Tree
- Use `nearest()` and `closest()` for dynamic interactions
- Leverage event delegation
- Avoid unstyled content flashes

### State Management
- Store state in DOM attributes (data-*)
- Let Hyperclay persist changes automatically
- Use hidden elements for non-visual state

## Security Model

Hyperclay trusts app owners to manage their own code and content, similar to WordPress. Content that is illegal or harmful is reported and removed.

## Philosophy

> "Write a few lines of JS + HTML, Hyperclay handles persistence and access control, you get a great app with 0 time spent fiddling with web services."

## Local Development Notes

When developing locally (not on Hyperclay platform):
- The Starter Kit script is NOT available via CDN
- Must implement persistence manually (localStorage, etc.)
- Can still follow Hyperclay patterns (DOM as database)
- Deploy to Hyperclay platform to get automatic features
