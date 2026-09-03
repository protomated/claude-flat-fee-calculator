# Connectors

This plugin uses a connector that ships with Claude Desktop, managed by Anthropic — you do not need to set up OAuth credentials.

## Connector for this plugin

| Connector | What it does | Setup |
|---|---|---|
| **Filesystem** | Optionally cross-checks time estimates against saved billing-narrative output; saves the CSV model only with your explicit confirmation | Connect once via Claude Desktop → Connectors → Filesystem → "Connect" then select your matters folder |

## Privacy note

All data read from your connected sources is processed within your Claude Desktop session, under your Claude plan's data handling terms. Nothing is transmitted to Protomated or any other third party.

## Troubleshooting

**Filesystem shows "Permission denied" or can't find a file:**
The file is likely outside your allowed folder. Go to Settings → Connectors → Filesystem and verify the path you selected.

**CSV won't open cleanly in Excel:**
Make sure you saved it with the `.csv` extension the skill proposes. If a currency or percentage column looks like plain text instead of a number, re-import it or use your spreadsheet program's "convert text to columns" tool.
