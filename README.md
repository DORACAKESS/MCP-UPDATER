# MCP-UPDATER

Dedicated Over-The-Air (OTA) Differential Update Repository for [MCP Manager](https://github.com/DORACAKESS/MCP-ARENA).

## 📌 What is this repository?
This repository is an automated distribution endpoint that serves lightweight differential packages (`<5MB`) for existing MCP Manager desktop installations.

- **Primary Repository & Full Installers**: [DORACAKESS/MCP-ARENA](https://github.com/DORACAKESS/MCP-ARENA)
- **Differential OTA Channel**: [DORACAKESS/MCP-UPDATER](https://github.com/DORACAKESS/MCP-UPDATER)

## 🚀 How it Works
1. When a new release is built, `mcp-update-differential.zip` (0.41 MB) and `app.asar` (3.98 MB) are deployed to this repository.
2. The MCP Manager desktop application checks for updates.
3. If local binaries are intact (verified via SHA-256 pre-scan), the app downloads the ~0.4MB differential archive from this repository and hot-swaps seamlessly in less than 2 seconds.
4. If local binaries are damaged or missing, the app automatically diverts to downloading the full installer from `MCP-ARENA`.
