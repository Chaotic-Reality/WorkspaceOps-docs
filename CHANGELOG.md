# WorkspaceOps release notes

WorkspaceOps is in development. These notes describe development builds, not browser-store availability. Live Chrome and Edge acceptance remains a release gate.

## 0.3.2

- Import JSON/YAML as copies, replacements, or merges after choosing destinations and reviewing before/after counts.
- Imports save as one operation. A destination changed since review blocks the entire import, preserving the latest saved data.
- Replacements retain the destination identity and use imported contents. Merges preserve every window, group, and duplicate tab.

## 0.3.1

- Manager shortcuts: / focuses search, Alt+Shift+C captures, and Alt+Shift+R restores the single selected workspace after confirmation. Shortcuts pause while typing or using dialogs.
- Group emoji picker and locally generated workspace previews. No page images are fetched.

## 0.3.0

- Merge into an existing workspace with a preview, revision protection, and safe undo.
- Select multiple workspace cards for combine and export.
- Favorites and Recently opened views, stored locally and separately from exports.
- An About page with version, ownership, privacy information, documentation, and issue links.
- Collections, appearance settings, storage usage, and collapsible navigation.
- Clean/Modern styles, light/dark/system colors, custom accents, and density controls. See [appearance notes](APPEARANCE.md).

## 0.2.3

- Move product documentation and the roadmap to this public repository.

## 0.2.2

- Dotted insertion indicators show where dragged groups and tabs will land.

## 0.2.1

- Collapse and expand groups in the editor.
- Automatic scrolling during dragging and a fixed drop target for the last group position.

## 0.2.0

- Nested group editing, keyboard movement, and drag-and-drop ordering.
- Nested JSON/YAML exports with support for legacy imports.
- Combine workspaces and add templates to existing workspaces.
- Blue-grey styling and sidebar shortcuts.
