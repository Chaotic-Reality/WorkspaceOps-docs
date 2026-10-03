# ROVER Workspaces upgrade roadmap

Priority order agreed from the product discussion. Checked items are implemented with automated verification; live browser release acceptance remains a separate gate; an unchecked item is still pending. Chrome and Edge are the supported release targets. Owned by Chaotic-Reality. This documentation is public; application source remains private. Plans may change and do not promise delivery dates.

## 1. Group-first organization and portable data — implemented; live acceptance pending

- [x] Show each group with its tabs nested directly underneath.
- [x] Create a group, then add tabs within it.
- [x] Drag groups as a block; reorder tabs and move them between groups/windows.
- [x] Provide keyboard alternatives for moving groups and tabs.
- [x] Editor collapse/expand controls, drag auto-scroll, and a fixed last-position drop target.
- [x] Preserve pinned tabs, active tabs, group colors, and collapsed state.
- [x] Export JSON/YAML as nested groups with their tabs; continue importing legacy files.
- [x] Verify save, reload, export/import, and restore ordering without losing existing data.
- [x] Add an automated full-cycle regression check for JSON and YAML, covering multiple windows, pinned tabs, interleaved ungrouped tabs, active tabs, and group properties. Live browser acceptance remains pending.

## 2. Combine workspaces

- [x] Select multiple workspaces and preview a new combined workspace.
- [x] Keep all source workspaces intact.
- [x] Choose whether to preserve source windows, use one window per source workspace, or combine into one window.
- [x] Choose whether same-name groups stay separate, receive distinct names, or merge.
- [x] Report duplicate URLs; let the user decide whether to remove them.
- [x] Add safe undo for the newly combined result.
- [x] Merge into an existing workspace with a before/after preview, revision checks, and undo while the result is unchanged.

- [x] Starter templates: Add to workspace with existing/new window selection, preview, group conflict choices, and stale-save protection.

## 3. Useful left navigation

- [x] Replace decorative sidebar space with working navigation and actions.
- [x] Show workspace count and quick capture.
- [x] Add multi-select actions for combine and export.
- [x] Add Favorites and Recently opened views.
- [x] Add Templates navigation.
- [x] Link the prioritized roadmap from the bottom of the sidebar.
- [x] Add an About page with version, ownership, privacy/storage details, support, and release notes.
- [x] Add collections (for example Personal, Work, Projects), separate from tab groups.
- [x] Place Appearance, Settings, and local storage status in the sidebar.
- [x] Make the rail collapsible and use a drawer or top navigation at narrow widths.

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

- [x] Clean mode: restrained layout, compact cards, muted surfaces.
- [x] Modern mode: stronger hierarchy, richer cards, subtle depth, optional motion.
- [x] Preset accent colors and custom color selection.
- [x] Light/dark support with accessible text, focus, and selected states.
- [x] Compact/comfortable density controls.
- [x] Respect reduced-motion preferences.
- [x] Persist preferences separately from workspace exports.
- [x] Investigate browser profile colors: no documented supported API found. System light/dark and manual accent selection are provided; see [appearance notes](APPEARANCE.md).

## 6. Faster everyday use

- [x] Keyboard shortcuts for capture, search, and restore within the manager.
- [x] Custom group emojis, including a picker and typed/pasted emoji names.
- [ ] Add a privacy-safe icon library for workspace groups, with bundled icons and optional local favicon resolution; external icon APIs must be explicitly opt in.
- [x] Workspace thumbnails generated locally from group colors/titles.
- [x] Import conflict choices: add copy, replace, or merge with preview and atomic stale-destination protection.

## 7. Release readiness

This is a gate before public release, regardless of feature priority.

- [ ] Complete live Chrome and Edge acceptance testing for each released change.
- [x] Replace placeholder icons with blue-grey browser/group artwork at all required extension sizes.
- [ ] Verify icon appearance in installed Chrome/Edge and capture final listing screenshots.
- [x] Document current privacy/data handling and the public support channel; link them from About.
- [x] Add a plain-language privacy statement and proprietary application license statement.
- [x] Use consistent outline navigation/template icons and keep Roadmap/About together at the bottom of the sidebar.
- [x] Review bundled runtime dependency notices and enforce matching licenses/versioned notices during builds.
- [ ] Recheck final store disclosures and dependencies against the release candidate before submission.
- [x] Prepare draft store descriptions, permission explanations, and reviewer test steps; see [store listing preparation](STORE_LISTING.md). Submission remains pending.
- [x] Document versioning, rollback, and store submission steps; see [release process](RELEASING.md).
- [x] Include a package verification record with ZIP/file checksums and checkout details; keep browser acceptance explicitly separate.
- [ ] Decide monetization after validating the core experience; no billing secrets in extension code.
- [x] Prepare a private free/paid proposal; pricing and entitlements are not implemented or announced.
- [ ] Validate demand for optional automation, workspace version history, and opt-in sync before building paid tiers.

## 8. Next local workflow improvements

Agreed direction from the competitor review; implementation remains pending. Complete the release gate before public launch.

- [x] Search saved tab titles, URLs, domains, and groups; open individual results or all matches from a workspace card.
- [x] Restore selected tabs/groups and preview already-open duplicates, including an open-missing-only option.
- [x] Choose whether selected tabs/groups are added to the current window or opened in new window(s).
- [x] Offer open-missing-only restore with URL duplicate detection while preserving the existing full-workspace restore path.
- [x] Add recent local snapshots, revision comparison, and whole-revision recovery; selective tab/group recovery remains pending.
- [x] Capture individual tabs/groups through context-menu actions; toolbar capture remains available for full workspaces.
- [x] Preview imports from browser bookmark HTML and pasted URL lists; Toby-specific export mapping remains pending.
- [x] Reload the current browser window from a saved workspace while keeping the ROVER manager page open.
- [x] Let users choose whether a workspace opens in new windows or replaces the current window, with a saved default preference.
- [ ] Add reusable workspace recipes with user-supplied project values.
  - **Definition:** Let a user save a repeatable workspace recipe with placeholders such as project name, environment, or client. Applying a recipe should create or update a workspace after showing the resolved URLs and groups for review. Recipes remain local until an explicit sync feature exists.
- [ ] Preview local organization rules and duplicate cleanup.
  - **Definition:** Provide a dry-run view of local rules that identify duplicate URLs, stale tabs, empty groups, and naming inconsistencies. The user must review proposed changes before anything is removed, merged, renamed, or moved.
- **Next decision:** Selective tab/group restore remains the next implementation candidate. It should let a user choose specific windows, groups, or tabs from a restore preview and show which existing tabs would be skipped before opening anything.
- [x] Simplify workspace cards: put title beside selection, remove duplicate visual previews, and let users choose how many group chips appear.
- [x] Reorder workspace cards with drag-and-drop and persist the order locally.
- [x] Add direct card actions for opening in the current window or new window(s), alongside selective restore and reload.

## 9. Launch learning and feedback

These are future capabilities. The current extension does not upload surveys, feedback, or usage data.

- [ ] Offer a short, skippable onboarding survey about intended use and desired capabilities; separate local preferences from explicitly submitted research answers.
- [ ] Offer a feedback prompt after several days of actual use, with Later and Do not ask again choices; keep feedback available in About.
- [ ] Provide a private feedback submission channel, optional reply email, and clear data/retention disclosures before enabling collection.
- [ ] Evaluate a low-cost submission service with abuse protection, restricted administrative access, deletion support, and operating limits.
- [ ] Evaluate clearly labeled, non-personalized sponsorship for Free; do not use survey answers, workspace contents, or browsing activity for personalized ads. Review both stores' policies before implementation.

## 10. Far-future profile sync and team features

- [ ] Evaluate browser sync after local workflows are stable.
- [ ] Introduce user-named ROVER Workspaces profiles such as Personal and Work, with explicit mapping of each browser installation/profile to a sync profile.
- [ ] Support opt-in cross-browser/device cloud sync without automatically merging profiles based on matching names or email addresses.
- [ ] Design profile isolation, conflict handling, device unlinking, encryption/key recovery, and deletion before enabling sync.
- [ ] Evaluate OneDrive/SharePoint sync and shared team workspaces.
- [ ] Add other browsers only when customer demand and market share justify the maintenance cost.

## Working approach

Finish and verify one feature milestone at a time. Commit each milestone, then let GitHub Actions check it. Treat suggested enhancements as planned work, not as existing capabilities. Retain existing user workspaces throughout upgrades.
