# Role 02_hardening

## Purpose
This role strengthens the operating system hosting the Geth node based on PCI-DSS requirements.

### Key Features
- Lock root password and manage sudo privileges
- Enforce strong password policy (minlen=12, rotation=90d)
- Secure SSH configuration
- Apply UFW firewall rules
- Kernel-level hardening via sysctl
- Enable optional 2FA using Google Authenticator

### PCI-DSS Mapping
| Control | Description |
|----------|-------------|
| Req 1 | Restrict inbound/outbound traffic using firewall |
| Req 2 | Harden kernel and remove insecure services |
| Req 6 | Maintain secure configurations |
| Req 8 | Enforce user authentication & access control |
| Req 10 | Log authentication attempts |
| Req 11 | Enable periodic testing & 2FA |

### Variables
- `privileged_group`: sudo group name (default: `devops`)
- `trusted_controller_ip`: IP allowed for RPC (default: `192.168.0.112`)

