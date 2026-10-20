# Pi-hole and DNS

## Last documented state

The working installation is a Pi-hole VM under VirtualBox on the Intel NUC. An attempted Ubuntu Desktop VM deployment on Proxmox was rolled back in favor of that working installation.

## Migration attempt

The Ubuntu guest showed conflicting address configuration: DHCP and a manually assigned address appeared together, and the GUI reverted to automatic configuration. Netplan configuration using NetworkManager and a `dhcp4` setting were part of the investigation. DNS settings and loopback addresses also needed to be distinguished from the guest's LAN identity.

The attempt did not establish a stable replacement. The public record preserves the rollback outcome instead of describing the migration as successful.

## Lessons

- Identify which component manages an interface before editing multiple configuration layers.
- Confirm the effective address, route, and DNS configuration after each change.
- A loopback address is not the VM's LAN address.
- A reachable IP does not prove that DNS resolution works.
- Keep the original DNS service available until a replacement passes client checks.
- Verify the DNS server actually used by clients after any fallback or rollback.

No query logs, client names, blocklist exports, private addresses, or admin credentials are included.
