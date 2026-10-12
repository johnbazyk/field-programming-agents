# Windows 10 Field Kit Configuration

The host computer must be configured so that:
- Cellular is the **only** default route for internet traffic.
- The local Ethernet interface reaches **only** the isolated camera / device subnet.
- Host firewall restricts local traffic to expected device IPs and ports.
- No residual credentials, configs, or routes remain after a job.

## Required Configuration

### Networking
1. Name adapters clearly (e.g., `Cellular`, `CameraNet`).
2. Cellular interface: sole default gateway. Low interface metric.
3. Local Ethernet: **no default gateway**. Static IP on the camera subnet only. Higher metric.
4. Confirm only one 0.0.0.0 route (via Cellular).
5. Disable unused radios.

### Firewall
- Windows Defender Firewall enabled.
- Local interface outbound only to the target camera subnet and required ports.
- Block all other traffic from the local interface.

### Security & Hygiene
- Full-disk encryption (BitLocker).
- No persistent credentials on the kit.
- Clean residual routes, profiles, and browser data after each job.

### Phase 0 Verification
- Default route is Cellular only.
- Local interface cannot reach the internet or other subnets.
- Firewall rules are active and restrictive.
- No leftover passwords or configuration from previous jobs.

Document results before any programming work begins.