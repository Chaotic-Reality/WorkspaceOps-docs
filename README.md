# WorkspaceOps

Save, organize, and restore browser workspaces with groups and tabs arranged the way you work.

WorkspaceOps is in development for Microsoft Edge and Google Chrome. Store availability has not been announced. This repository contains public product documentation; application source and development history remain private.

## Documentation

- [Prioritized roadmap](ROADMAP.md): completed features, upcoming improvements, and release gates.
- [About WorkspaceOps](ABOUT.md): ownership, privacy, and product boundaries.
- [Release notes](CHANGELOG.md): changes in development builds.
- [Appearance](APPEARANCE.md): styles, colors, and browser theme limitations.
- [Import guide](IMPORTING.md): copy, replace, merge, and conflict protection.
- [Release process](RELEASING.md): CI, packages, acceptance, versioning, and recovery.
- [Privacy and data handling](PRIVACY.md): local records, permissions, exports, and deletion.
- [Support](SUPPORT.md): reporting problems without exposing private workspace data.
- [Store listing preparation](STORE_LISTING.md): draft descriptions, permission explanations, and reviewer test steps; not submitted.

## Current capabilities

- Capture browser windows, tabs, pinned tabs, and tab groups.
- Create and edit workspaces with nested groups, drag-and-drop ordering, and keyboard controls.
- Restore saved workspaces into new windows without closing existing tabs.
- Import and export JSON or YAML, with tabs nested inside their groups.
- Combine workspaces with a preview and optional duplicate removal.
- Create workspaces from starter templates or add templates to existing workspaces.
- Organize with favorites and collections; revisit recently opened workspaces.
- Choose Clean/Modern styles, system/light/dark colors, custom accents, and density.
- Use group emojis, local previews, and manager keyboard shortcuts.

Features have automated coverage; live Chrome and Edge acceptance testing remains a release gate. Roadmap items are plans, not delivery commitments.

Please do not include private workspace exports, browsing history, credentials, or sensitive URLs in public issues.

© Chaotic-Reality. Publication of these documents does not grant a license to the application source code.
