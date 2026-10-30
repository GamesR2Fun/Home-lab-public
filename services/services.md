# Services Overview

This is the public service inventory. It focuses on what each service does, why it exists, and how it fits into the lab without publishing access details or sensitive configuration.

## Core infrastructure

| Service / Platform | Status | Role |
| --- | --- | --- |
| Proxmox VE | Current | Primary VM and container platform |
| OPNsense | Current | Routing, firewalling, and network control |
| Active Directory / DNS | Current | Centralized Windows identity and local name services |
| Samba / SMB | Current | Shared file access to locally hosted storage |
| ZFS storage | Current | Redundant storage for system, VM/container, and bulk-data workloads |
| Managed switching | Current | LAN connectivity and network segmentation foundation |

### Proxmox VE

The main compute platform for the Home Lab. Most infrastructure is separated into VMs and Linux containers so services can be maintained, backed up, and rebuilt independently.

### OPNsense

Provides the primary firewall and routing layer. Detailed rules, interfaces, addressing, and remote-access configuration are intentionally private.

### Active Directory / DNS

Provides identity, authentication, local DNS, and supporting Windows domain services for systems that benefit from centralized management.

### Samba / SMB

Provides Windows-compatible access to shared storage from a Debian-based file-service layer.

## Media and automation

| Service | Status | Role |
| --- | --- | --- |
| Jellyfin | Current | Primary media streaming platform |
| Sonarr | Current | TV and episodic-media automation |
| Radarr | Current | Movie automation |
| Prowlarr | Current | Centralized indexer management |
| Recyclarr | Current | Quality-profile and custom-format synchronization |
| qBittorrent | Current | Remote download client hosted off-site |
| rclone | Current | Controlled remote-to-local transfer workflow |
| Portainer | Current | Graphical Docker management |
| Immich | Current / Evolving | Self-hosted photo and video management |

### Jellyfin

Jellyfin is the primary media server and uses an NVIDIA Tesla P4 for supported hardware-accelerated video processing.

The library spans television, movies, anime, music, and archival/older media. Hardware acceleration reduces the amount of CPU work required when clients need transcoding.

### Sonarr and Radarr

Sonarr and Radarr manage media availability, quality targets, downloads, imports, naming, and library organization for TV/episodic content and movies respectively.

### Prowlarr

Acts as the centralized indexer-management layer for the media automation stack so individual applications do not need completely separate indexer administration.

### Recyclarr

Keeps selected quality profiles and custom-format preferences consistent across the Arr applications.

### qBittorrent on Ultra.cc

Download activity is handled remotely rather than directly on the local media server. This keeps acquisition and seeding workloads separated from the local library and playback infrastructure.

### rclone

Moves completed media from the remote acquisition environment into local storage through a controlled staging/import workflow.

### Immich

Provides self-hosted photo/video organization with modern features such as timeline browsing, metadata processing, and face recognition.

The Immich project is still evolving as older media collections are cleaned up and imported.

## Operations, tooling, and documentation

| Service / Tool | Status | Role |
| --- | --- | --- |
| Portainer | Current | Docker and container-management interface |
| Jellyfin troubleshooting integration | Current | Scoped read-only diagnostic access to Jellyfin logs |
| Obsidian + GitHub | Current | Private Home Lab documentation platform |
| Automated documentation review | Current / Evolving | Helps compare recent work against maintained documentation |
| Uptime monitoring | Current | Basic service availability monitoring |

### Documentation platform

The private documentation repository is treated as the authoritative knowledge base for the lab. It contains the detailed system state, runbooks, troubleshooting, diagrams, architecture decisions, and roadmap.

This public repository is a separate, sanitized summary and intentionally does not mirror every change.

## In progress

| Service / Project | Goal |
| --- | --- |
| Proxmox Backup Server | Dedicated backup and restore platform with validated recovery |
| qBittorrent lifecycle management | Safe cleanup after transfer, import, retention, and seeding requirements are satisfied |
| Health monitoring / notifications | Better visibility into service and infrastructure health |
| Public Home Lab documentation | Sanitized, shareable project overview |
| Photo/video organization | Continue deduplication, classification, and Immich ingestion |

### Backup platform

The backup project is focused on reducing overlapping backup approaches and replacing them with a simpler, better-tested recovery model.

Proxmox Backup Server is part of the target design, but it will not be considered complete until restores are proven.

### qBittorrent lifecycle management

Remote cleanup is being approached conservatively. The goal is to automatically remove completed remote data only when the system can prove the content was transferred, imported, retained locally, and satisfied required seeding conditions.

Development begins in report-only mode before any destructive behavior is enabled.

### Monitoring and notifications

The lab is moving toward broader visibility into host health, services, storage, media playback, transfers, backups, networking, and GPU utilization.

## Planned

| Service / Project | Goal |
| --- | --- |
| Jarvis local-AI server | Dedicated GPU-backed local AI and automation platform |
| Homarr | Unified Home Lab dashboard |
| Bazarr | Subtitle automation |
| Seerr | Media request management |
| Huntarr | Missing-content and quality automation |
| autobrr | Torrent announcement and automation tooling |
| Expanded monitoring | Storage, media, networking, transfer, backup, GPU, and service-health visibility |
| Improved restore testing | Repeatable validation that backups can actually be recovered |

### Jarvis

Jarvis is planned as a dedicated local-AI system rather than a single application.

The long-term direction includes:

- Home Lab knowledge retrieval
- Log analysis and troubleshooting assistance
- Controlled infrastructure actions
- Smart-home integration
- Workshop voice assistance
- Camera-assisted tool/object location
- Interactive build and repair guidance

### Homarr

Planned as a central visual dashboard for selected service links and high-level status information.

### Bazarr, Seerr, Huntarr, and autobrr

These tools are planned to fill specific gaps in the existing media stack: subtitles, requests, missing/quality management, and torrent automation.

They are not considered deployed until implementation and validation are complete.

## Publication policy

This inventory intentionally excludes:

- Hostnames and private addresses
- Internal ports and access URLs
- Credentials and API tokens
- Exact storage/share paths
- Firewall and VPN configuration
- Backup destinations
- Sensitive logs and raw production configuration

Those details belong only in the private operational documentation.
