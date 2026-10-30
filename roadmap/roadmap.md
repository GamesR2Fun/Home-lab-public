# Public Roadmap

This roadmap is intentionally higher-level and slower-moving than the private operational backlog.

## Now

- **Backup redesign / Proxmox Backup Server** — preparing storage and recovery strategy before full deployment.
- **qBittorrent lifecycle management** — validating safe cleanup logic in report-only mode before enabling destructive actions.
- **Monitoring and notifications** — expanding visibility into service and infrastructure health.
- **Public Home Lab documentation** — building this sanitized repository for safe sharing.

## Next

- **Jarvis local-AI server** — build the initial dedicated GPU-backed system and establish the software platform.
- **Homarr dashboard** — centralize service links, status, and selected monitoring data.
- **Bazarr** — add subtitle automation.
- **Seerr** — add media request management.
- **Huntarr** — improve missing-content and quality automation.
- **autobrr** — evaluate and add torrent announcement automation where useful.

## Later

- Expand Jarvis beyond Home Lab administration into workshop and smart-home assistance.
- Add broader storage, network, transfer, stream, and service-health monitoring.
- Improve backup testing, restore validation, and documentation around disaster recovery.
- Continue refining the media automation pipeline as new tools prove useful and maintainable.

## Done highlights

- Migrated the primary Home Lab platform to Proxmox VE.
- Built ZFS-backed storage tiers for system, VM/container, and bulk media workloads.
- Deployed Jellyfin with NVIDIA hardware acceleration.
- Built the Sonarr/Radarr/Prowlarr/Recyclarr automation stack.
- Implemented the Ultra.cc + qBittorrent + rclone remote acquisition workflow.
- Deployed Immich for photo/video management.
- Established GitHub + Obsidian as the private operational documentation platform.
- Added scoped read-only Jellyfin troubleshooting access for AI-assisted diagnostics.

## Notes

Items appear here only when they are appropriate to disclose publicly. Detailed implementation tasks, blockers, addresses, credentials, access paths, and troubleshooting evidence remain private.
