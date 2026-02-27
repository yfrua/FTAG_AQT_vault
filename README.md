# FTAG_AQT_vault

An [Obsidian](https://obsidian.md/) note backup repository.

## About

This repository serves as a backup for the FTAG_AQT Obsidian vault. It stores notes and configurations tracked with Git to enable version history and recovery.

## Usage

### Initial Setup

1. Clone this repository into your local Obsidian vaults folder:
   ```bash
   git clone https://github.com/yfrua/FTAG_AQT_vault.git
   ```
2. Open the cloned folder as a vault in Obsidian.

### Syncing Changes

To back up your latest notes, commit and push your changes:

```bash
git add .
git commit -m "Update notes"
git push
```

### Restoring Notes

To restore notes on a new device, clone the repository and open the folder in Obsidian.

## Structure

```text
FTAG_AQT_vault/
├── .obsidian/          # Obsidian configuration (themes, plugins, settings)
├── Notes/              # Research notes and documentation
├── attachments/        # Images and media files
└── README.md           # This file
```

## Content Overview

The vault currently contains research notes focused on FTAG (Flavour Tagging) and jet calibration:
- **Light-jet calibration**: Investigating methods for calibrating GN3 light-jet efficiency using di-jet samples and negative-tag methods.
- **Presentations**: Documentation of presentations and meetings (e.g., Ellen's presentations).

## Notes

- The `.obsidian/workspace.json` file is excluded from tracking as it contains per-device window state.
- Plugin data stored under `.obsidian/plugins/` is tracked to preserve plugin configurations.
