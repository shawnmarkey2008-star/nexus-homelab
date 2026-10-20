# Remote access and operations

## Administration

Tailscale and Remote Desktop were used for private administration. The desktop Launchpad provides convenient entry points to dashboards, SSH, scripts, folders, and Windows Remote Desktop. It does not replace network access or authentication.

The private command-center site organized inventory, topology, dependencies, and unresolved questions. Its recorded status was documentation, not live telemetry. The public GitHub write-up follows the same distinction.

## Practices developed through the project

1. Separate observed behavior from assumptions and plans.
2. Record a working baseline before migrations.
3. Verify a local service before debugging its remote route.
4. Change one layer at a time when diagnosing networking.
5. Keep a rollback path for shared services such as DNS.
6. Document dependencies so host restarts have predictable consequences.

## Public documentation boundaries

Public material uses role names and examples. Real management addresses, private DNS names, Tailscale device details, switch dumps, tokens, device serial numbers, screenshots of private dashboards, and personal records remain outside this repository.
