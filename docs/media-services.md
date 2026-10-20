# Jellyfin and Cloudflare Tunnel

## Documented implementation

Jellyfin runs on the Windows-based Intel NUC and uses external media storage. A Cloudflare Tunnel connector on the NUC provides the remote service route. The project included moving the service from an earlier custom domain to a new one and updating the root and `www` routing entries.

Real domains, tunnel identifiers, credential files, and media-library contents are excluded from this public write-up.

## Request path

Remote client requests reach the configured Cloudflare hostname, traverse the tunnel connector, and reach the local Jellyfin origin. Local access can reach the origin directly. A healthy local origin does not guarantee that the external path is healthy.

## Validation approach used

1. Check the local Jellyfin interface and its `/health` endpoint.
2. Check the external service route independently.
3. Confirm that the hostname maps to the intended origin.
4. Compare browser behavior and dedicated-client behavior when only one fails.

Client-side filtering, DNS, TLS, authentication, and connectivity can affect the external path. The record contains remote-client troubleshooting, but does not establish a universal cause for every failed client connection.

## Learning outcomes

Separating origin health from remote-route health made failures easier to locate. The work also reinforced that changing DNS names, tunnel routing, and client configuration are separate steps. This is a record of the project, not a recommendation that a particular provider configuration or service plan supports every media workload.
