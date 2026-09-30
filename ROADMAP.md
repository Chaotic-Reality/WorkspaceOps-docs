# WorkspaceOps upgrade roadmap

Priority order agreed from the product discussion. Checked items are implemented with automated verification; live browser release acceptance remains a separate gate; an unchecked item is still pending. Chrome and Edge are the supported release targets. Owned by Chaotic-Reality. This documentation is public; application source remains private. Plans may change and do not promise delivery dates.

## 1. Group-first organization and portable data — implemented; live acceptance pending

- [x] Show each group with its tabs nested directly underneath.
- [x] Create a group, then add tabs within it.
- [x] Drag groups as a block; reorder tabs and move them between groups/windows.
- [x] Provide keyboard alternatives for moving groups and tabs.
- [x] Editor collapse/expand controls, drag auto-scroll, and a fixed last-position drop target.
- [x] Preserve pinned tabs, active tabs, group colors, and collapsed state.
- [x] Export JSON/YAML as nested groups with their tabs; continue importing legacy files.
- [ ] Verify save, reload, export/import, and restore ordering without losing existing data.

## 2. Combine workspaces

- [x] Select multiple workspaces and preview a new combined workspace.
- [x] Keep all source workspaces intact.
- [x] Choose whether to preserve source windows, use one window per source workspace, or combine into one window.
- [x] Choose whether same-name groups stay separate, receive distinct names, or merge.
- [x] Report duplicate URLs; let the user decide whether to remove them.
- [x] Add safe undo for the newly combined result.
- [ ] Later: merge into an existing workspace with conflict preview, revision checks, and undo.

- [x] Starter templates: Add to workspace with existing/new window selection, preview, group conflict choices, and stale-save protection.

## 3. Useful left navigation

- [x] Replace decorative sidebar space with working navigation and actions.
- [x] Show workspace count and quick capture.
- [ ] Add multi-select actions for combine and export.
- [ ] Add Favorites and Recently opened views.
- [x] Add Templates navigation.
- [x] Link the prioritized roadmap from the bottom of the sidebar.
- [ ] Add an About page with version, ownership, privacy/storage details, support, and release notes.
- [ ] Add collections (for example Personal, Work, Projects), separate from tab groups.
- [ ] Place Appearance, Settings, and local storage status in the sidebar.
- [ ] Make the rail collapsible and use a drawer or top navigation at narrow widths.

## 4. Default blue-grey / blue-black design

This is the selected default direction. The proposed starting colors below must be checked in context for readable contrast; focus indicators may need a darker tone.

| Role                     | Starting color |
| ------------------------ | -------------- |
| Page background          | #F3F6F8        |
| Surface/card             | #FFFFFF        |
| Primary text             | #1F2933        |
| Secondary text           | #607080        |
| Borders                  | #D5DEE5        |
| Primary blue             | #315C86        |
| Deep blue-grey / sidebar | #243B53        |
| Hover blue               | #274C70        |
| Soft blue highlight      | #E6EFF7        |
| Focus ring               | #315C86        |

- [x] Extract interface colors into reusable design tokens.
- [x] Apply the blue-grey default across the interface.
- [x] Preserve independent browser tab-group colors.

## 5. Appearance preferences

- [ ] Clean mode: restrained layout, compact cards, muted surfaces.
- [ ] Modern mode: stronger hierarchy, richer cards, subtle depth, optional motion.
- [ ] Preset accent colors and custom color selection.
- [ ] Light/dark support with accessible text, focus, and selected states.
- [ ] Compact/comfortable density controls.
- [ ] Respect reduced-motion preferences.
- [ ] Persist preferences separately from workspace exports.
- [ ] Investigate inheriting browser profile colors in Chrome and Edge; do not promise this until a reliable supported mechanism is confirmed. Provide a fallback.

## 6. Faster everyday use

- [ ] Keyboard shortcuts for capture, search, and restore.
- [ ] Custom group icons or emojis.
- [ ] Workspace thumbnails generated locally from group colors/titles.
- [ ] Import conflict choices: add copy, replace, or merge with preview.

## 7. Release readiness

This is a gate before public release, regardless of feature priority.

- [ ] Complete live Chrome and Edge acceptance testing for each released change.
- [ ] Final icons, screenshots, privacy disclosures, support contact, and dependency review.
- [ ] Document versioning, rollback, and store submission steps.
- [ ] Decide monetization after validating the core experience; no billing secrets in extension code.

## 8. Optional cloud and team features

- [ ] Evaluate browser sync after local workflows are stable.
- [ ] Evaluate OneDrive/SharePoint sync and shared team workspaces.
- [ ] Add other browsers only when customer demand and market share justify the maintenance cost.

## Working approach

Finish and verify one feature milestone at a time. Commit each milestone, then let GitHub Actions check it. Treat suggested enhancements as planned work, not as existing capabilities. Retain existing user workspaces throughout upgrades.

