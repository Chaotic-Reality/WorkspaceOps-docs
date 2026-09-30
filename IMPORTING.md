# Importing workspaces

Choose **Import file**, select a JSON or YAML export, then review each workspace before saving. Importing saves workspace data; it does not open browser tabs.

| Choice              | What happens                                                                                                                                          |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Add copy (default)  | Creates an independent workspace. Duplicate names receive an imported suffix.                                                                         |
| Replace existing    | Uses the imported name, description, windows, groups, and tabs. Keeps the destination's identity, creation date, favorite, and collection assignment. |
| Merge into existing | Keeps the destination's name and description and appends imported windows. Preserves groups and duplicate tabs.                                       |

Replace and merge require an explicit destination. Each destination can be used only once per file import. Before/after window, group, and tab counts appear before saving. Export a backup before replacing contents you may want later; replacement does not have a dedicated Undo action.

All items save together. If another manager changes or removes a destination after the preview, the entire import is rejected. Cancel, reopen the file, and review the current destination before trying again. Workspace limits still apply, including to merged results.

Exports use the nested version 2.0 format. Legacy version 1.0 files remain supported. Files must fit the 2 MB import limit and pass validation. Imported data stays in local extension storage; it is not uploaded by WorkspaceOps.

This describes development builds starting at 0.3.2. Installed Chrome and Edge acceptance remains pending.
