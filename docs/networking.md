# Networking and VLANs

## Work completed

The networking project used a Cisco Catalyst 2960-X with a Netgear R6230 and the Xfinity ISP connection. Switch sections were assigned roles for upstream connectivity, the main lab, an experimental router/firewall segment, and spare capacity.

The upstream feed and Netgear WAN share the upstream segment. The Netgear LAN feeds the lab segment. Keeping these roles distinct is essential when recabling the switch.

Serial-console access from a Mac and inspection of interface state were part of the work. Link speed, negotiated duplex, and connected ports were examined while diagnosing slow connectivity.

## Read-only inspection commands used

```text
terminal length 0
show interfaces status
show interfaces status | include connected
```

These are inspection commands, not a configuration restore. Interface names and output vary by device and software.

## What remains unverified

Earlier records and later conversational shorthand do not consistently identify VLAN numbers. The roles above are documented; an exact current port/VLAN table is deliberately withheld until a fresh configuration is available. No running configuration, management address, credentials, or serial-console device identifier is published.

Cisco router and SonicWall configuration was not confirmed complete. They are not presented as a deployed firewall design.

## Lessons

- Record both ends of each cable before changing several connections.
- Check the physical link and negotiated speed before changing DNS or VM settings.
- A router web page loading slowly and a host being unreachable are different symptoms.
- VLAN membership alone does not provide routing or prove that a firewall policy is correct.
- Preserve a known working access method while changing management connectivity.
