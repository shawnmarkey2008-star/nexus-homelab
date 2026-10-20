# Virtualization

## Proxmox host

A Dell OptiPlex provides the home virtualization platform. Documented guests include Home Assistant OS and Windows Server. The Windows Server VM provides a platform for Windows administration and domain-service learning; a complete, verified domain deployment is not claimed here.

Home Assistant runs as its own guest. Restarting a desktop used to administer the host does not inherently stop a VM running on Proxmox; the guest's lifecycle belongs to the host.

## VirtualBox on the NUC

The NUC also runs a Pi-hole VM under VirtualBox. This remained the working DNS setup after the attempted Proxmox migration. Maintaining a functional existing VM provided a rollback path.

## Operational considerations learned

- Distinguish the hypervisor address from guest addresses.
- A browser or remote-desktop client is an administration interface, not the VM itself.
- Host restarts affect every service depending on that host.
- Guest network mode, DNS configuration, and static address ownership need to agree.
- Clipboard sharing is a separate guest-integration problem and does not fix networking.

No private VM exports, disk images, Windows product keys, or credentials are included. Backup and restore automation is not represented as completed without a recorded restore test.
