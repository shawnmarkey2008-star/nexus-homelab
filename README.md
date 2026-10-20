# Nexus Homelab

**Network for Experimentation, Utility and Storage.**

My personal lab for learning networking, virtualization, self-hosted services, and home automation. This repository documents how the pieces fit together and the lessons from building them.

This is a sanitized documentation snapshot prepared in October 2026, not a live status dashboard or a complete backup. Private addresses, public service endpoints, credentials, device identifiers, and raw configurations are omitted. Client jobs and employer/school environments are outside this repository.

## Explore

| Area | Documentation |
| --- | --- |
| Architecture and host roles | [Architecture](docs/architecture.md) |
| Cisco switching and VLANs | [Networking](docs/networking.md) |
| Proxmox, Windows Server, VirtualBox | [Virtualization](docs/virtualization.md) |
| Jellyfin and Cloudflare Tunnel | [Media services](docs/media-services.md) |
| HAOS, devices, and monitoring | [Home Assistant](docs/home-assistant.md) |
| Pi-hole and DNS migration | [DNS](docs/dns.md) |
| Remote access and operational lessons | [Operations](docs/operations.md) |

## Last documented state

- Intel NUC running Windows 11, Jellyfin, a Cloudflare connector, and a VirtualBox Pi-hole VM.
- Dell OptiPlex running Proxmox with Home Assistant OS and a Windows Server VM.
- Cisco Catalyst 2960-X providing separated switch segments around a Netgear router.
- Home Assistant integrating lighting/devices and tracking selected service availability.
- Pi-hole retained on VirtualBox after an unsuccessful migration attempt.
- A private command-center dashboard documenting inventory and dependencies. Its live source and private deployment are not included here.

The exact switch VLAN IDs and port assignments need fresh configuration evidence before publishing a reproducible configuration. Documentation describes their roles rather than asserting a current port map.

## Companion tools

- [Nexus Scanner](https://github.com/shawnmarkey2008-star/nexus.scanner): IPv4 host discovery and TCP checks.
- [Nexus Launchpad](https://github.com/shawnmarkey2008-star/nexus-launchpad): desktop shortcuts for lab tools and services.

## Skills practiced

Network segmentation, cabling and link diagnostics, virtual machines, local DNS, service publishing, Bluetooth passthrough, availability monitoring, and documenting dependencies.
