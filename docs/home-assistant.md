# Home Assistant

Home Assistant OS runs in a Proxmox VM and provides a central interface for smart-home devices and selected homelab checks.

## Documented work

- Nexus dashboard organization and a welcome description.
- Host availability checks for the NUC, Proxmox, and Windows Server VM.
- Separate local Jellyfin and external-route health checks.
- Hue Bluetooth bulbs with Bluetooth passthrough into the guest.
- Wyze camera/plug integration work and Alexa integration.
- A control for switching multiple Hue bulbs together.
- Mobile and remote dashboard access.

A Cisco switch ping check did not work during the recorded attempt and was skipped. It is not listed as verified monitoring.

## Lessons

Bluetooth hardware must be available to the guest that uses it. Device integration state, VM health, and network reachability are different layers. A Home Assistant update resolved a recorded brightness-control issue, while a plug power cycle restored a separate unavailable-lamp case.

Local service checks and external checks answer different questions. Their displayed names should make that distinction obvious.

## Public scope

This repository explains the implementation without distributing the private dashboard, camera feeds, location settings, tokens, entity inventory, or full Home Assistant backup. Exact YAML is not reconstructed from memory and presented as an exported working configuration.
