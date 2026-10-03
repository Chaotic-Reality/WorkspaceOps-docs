# How ROVER Workspaces works

ROVER Workspaces is a local Chromium extension for saving, organizing, and restoring groups of browser tabs. It stores workspace records in the current browser profile and only talks to the browser APIs when you capture, restore, import, or export.

## The simple flow

1. **Capture:** ROVER reads supported HTTP/HTTPS tabs and their groups.
2. **Organize:** You edit names, groups, order, collections, favorites, and Custom Templates.
3. **Save locally:** Workspace data stays in extension storage on your device.
4. **Restore:** ROVER creates windows and tabs, then rebuilds their groups.
5. **Export:** JSON and YAML files let you back up or move workspaces yourself.

The extension does not copy cookies, passwords, page contents, or authentication sessions. Browser-internal and private-window tabs are skipped during capture.

## Project tooling

The private application uses TypeScript for type checking, Vite for the Manifest V3 build, Vitest for tests, ESLint for code quality, Prettier for formatting, and GitHub Actions for repeatable checks and release artifacts. The public repository contains product documentation; the application source remains private.

## Where to learn more

- [User guide](https://github.com/Chaotic-Reality/rover-workspaces-docs/wiki/User-Guide)
- [Privacy and data handling](PRIVACY.md)
- [Import and export guide](IMPORTING.md)
- [Pricing and trial](PRICING.md)
- [Roadmap](ROADMAP.md)
