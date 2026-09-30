# Privacy and data handling

Last updated: September 30, 2026. Applies to the current local-only ROVER Workspaces development builds, owned by Chaotic-Reality. Store availability has not been announced.

## Our privacy statement

ROVER Workspaces helps you organize your tabs without sending your saved workspaces to us. The current extension keeps workspace information and preferences on your device. We do not receive, sell, or use that locally stored workspace data for advertising. No ROVER Workspaces account is required.

You choose when to capture, import, export, or open a workspace. Exporting creates a file you control; opening a workspace connects your browser to the saved websites. Information you voluntarily post in public support issues is separate from the extension's local data and is publicly visible on GitHub. The details below explain these boundaries and how to remove your local data.

## Data kept on your device

When you capture or save a workspace, ROVER Workspaces stores its name and description; supported HTTP/HTTPS tab URLs and titles; window and tab order; pinned and active state; group names, colors, and collapsed state; and workspace identifiers and creation/update times.

Favorites, collection names and assignments, and the last time a workspace was successfully opened are also stored locally. This recent-workspace record is not a record of every website you visit. Appearance preferences are stored separately. Local previews are drawn from saved group names and colors; ROVER Workspaces does not fetch screenshots or remote favicons for them.

These records use extension-local storage in the current browser profile. ROVER Workspaces does not provide its own encryption or a cloud backup. Other users or software with access to your device or profile may be able to access that data. Device backup software may also copy it.

## What the extension does not collect

The current implementation has no ROVER Workspaces account, analytics, advertising, crash-report upload, cloud synchronization, or server that receives saved workspaces. It does not read page content, cookies, passwords, form entries, or the browser's history database. It excludes private windows and browser-internal, file, and unsupported tab URLs when capturing.

URLs and titles can still contain personal information, search terms, private document names, or access tokens in query strings. Capture does not remove that information. Review saved data and exports before sharing them.

## Permissions and connections

| Permission | Current purpose                                                                              |
| ---------- | -------------------------------------------------------------------------------------------- |
| storage    | Save workspaces, organization, recent opens, and appearance preferences locally.             |
| tabs       | Read tab URLs/titles during capture and create, activate, pin, or group tabs during restore. |
| tabGroups  | Read group names/colors/collapsed state and recreate those properties.                       |

The manifest requests no host permissions and installs no content scripts. Capture is user initiated. Restoring opens the saved websites in new windows; those sites receive normal browser requests and follow their own privacy practices. Clicking documentation or support links opens GitHub, whose policies apply there. Browser and store services may have their own update or diagnostic behavior independent of ROVER Workspaces.

## Export, retention, and deletion

Exports are unencrypted JSON or YAML files containing workspace data. They do not include favorites, collections, recent-open records, or appearance settings. Exported files remain wherever your browser saves downloads until you remove them; deleting a workspace does not delete an exported copy.

Saved workspaces remain until you delete them or remove the extension's local data. Removing a collection only removes its organization; it does not delete the workspaces inside it. Uninstalling removes the extension's local data. Export anything you want to retain before uninstalling. Data copied to other devices, backups, exports, or websites must be managed separately.

## Questions and changes

Use the [support guide](SUPPORT.md) to contact the maintainer through the public project issue tracker. Do not post private exports, sensitive URLs, or credentials. Future account, sync, or monetization features would require this document and the corresponding store disclosures to be reviewed before release.
