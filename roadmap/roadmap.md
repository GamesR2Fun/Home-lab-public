# Public Roadmap

This roadmap is intentionally higher-level and slower-moving than the private operational backlog. It shows the direction of the lab without exposing implementation details that belong in the private documentation.

## Now

### Backup redesign / Proxmox Backup Server

The lab is moving toward a simpler backup architecture centered on Proxmox Backup Server.

Current focus:

- Freeing and preparing appropriate backup storage
- Reducing dependence on overlapping legacy backup methods
- Defining retention and recovery expectations
- Building restore validation into the process

The project will not be considered complete just because backup jobs run. Successful recovery testing is part of the finish line.

### qBittorrent lifecycle management

The current acquisition pipeline can transfer media successfully, but remote cleanup needs stronger proof before it becomes automatic.

Current focus:

- Verify content was fully transferred
- Confirm media was imported successfully
- Confirm the local library still contains the expected files
- Confirm seeding requirements are satisfied
- Avoid unsafe cleanup when evidence is incomplete

Development is intentionally starting with read-only/report-only evaluation before any automatic deletion is allowed.

### Monitoring and notifications

The monitoring strategy is being expanded from basic availability checks toward a broader operational view.

Target areas include:

- Server and service availability
- Storage health and capacity
- Network performance
- Media streams
- Transfer status
- Backup health
- GPU utilization
- Meaningful alerts without excessive notification noise

### Public Home Lab documentation

This repository is being built into a shareable overview of the lab.

The public view is intentionally separate from the private source-of-truth documentation so it can be updated less frequently and reviewed for privacy before publication.

### Photo/video organization

A large personal photo/video collection is being cleaned up and prepared for long-term management with Immich.

The work includes deduplication, categorization, metadata cleanup, and separating useful personal media from miscellaneous downloaded content.

## Next

### Jarvis local-AI server

Build the first dedicated local-AI server and establish the software platform.

Initial goals:

- Bring the GPU-backed server online
- Establish local model hosting
- Provide controlled access to Home Lab knowledge and tools
- Evaluate performance before adding additional GPU hardware
- Define safe permission boundaries for infrastructure actions

Longer term, Jarvis is intended to expand into smart-home and workshop assistance.

### Homarr dashboard

Build a central Home Lab dashboard that surfaces useful status information without requiring several separate interfaces.

Potential data includes:

- Service status
- Storage capacity/health
- Active media sessions
- Transfer status
- Recent media additions
- Network performance
- Host uptime

### Bazarr

Add subtitle automation to complement the existing Sonarr/Radarr workflow.

### Seerr

Add a user-friendly media request layer in front of the existing automation stack.

### Huntarr

Evaluate and deploy where useful for missing-content and quality-improvement workflows.

### autobrr

Evaluate torrent announcement automation and determine whether it adds enough value to justify the additional service.

## Later

### Expand Jarvis beyond infrastructure

Potential future capabilities include:

- Voice-triggered workshop assistance
- Smart-home control
- Camera-assisted object/tool location
- Build and repair guidance
- More autonomous Home Lab maintenance under scoped permissions

### Broader observability

Continue improving visibility across:

- Storage
- Network
- Transfers
- Media playback
- Backups
- GPU workloads
- Service health

### Backup maturity

Move from "backups exist" to routine confidence that recovery works.

Long-term goals include:

- Repeatable restore testing
- Clear recovery priorities
- Better disaster-recovery documentation
- Reduced dependency on one-off/manual recovery knowledge

### Media automation refinement

Continue improving the media stack as new tools prove useful and maintainable.

The goal is not to install every available Arr-related project; new services should fill a real gap or reduce manual work.

## Done highlights

### Proxmox migration

Moved the primary Home Lab onto Proxmox VE and established a VM/container-first architecture.

### ZFS storage redesign

Built separate ZFS-backed storage tiers for the hypervisor, VM/container workloads, and bulk data/media.

### Jellyfin production platform

Deployed Jellyfin as the primary media server with NVIDIA Tesla P4 hardware acceleration.

### Media automation stack

Built the Sonarr/Radarr/Prowlarr/Recyclarr stack and standardized the overall media-management workflow.

### Remote acquisition pipeline

Implemented the Ultra.cc + qBittorrent + rclone pipeline for remote acquisition, seeding, transfer, and local import.

### Immich deployment

Deployed Immich as the primary self-hosted photo/video management platform and began migrating organized media into it.

### Documentation platform

Moved operational Home Lab documentation into a private GitHub + Obsidian knowledge base designed for both human and AI-assisted maintenance.

### AI-assisted troubleshooting access

Added scoped read-only access to Jellyfin troubleshooting data so AI tools can inspect relevant logs without receiving unrestricted server access.

### Dad-Lab environment

Created a separated area of the virtualization environment for family lab use without mixing it directly into the main production workload set.

## Guiding principles

The roadmap follows a few recurring rules:

- Prefer maintainable, vendor-supported solutions where practical.
- Validate restores instead of assuming backups work.
- Keep destructive automation disabled until its safety conditions are proven.
- Add services because they solve a real problem, not just because they exist.
- Keep the Home Lab documented well enough that another person—or another AI session—can continue the work without relying on hidden context.

## Notes

Items appear here only when they are appropriate to disclose publicly. Detailed implementation tasks, blockers, addresses, credentials, access paths, and troubleshooting evidence remain private.
