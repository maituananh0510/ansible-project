# Role: 06_backup

## Purpose
Automate secure daily backups for Geth node and related configuration files.

## Tasks Summary
| Task | Purpose | Module |
|------|----------|--------|
| Ensure backup directory | Prepare secure storage for backups | `file` |
| Deploy backup script | Create and secure backup automation script | `template` |
| Schedule daily cron | Automate backup execution | `cron` |
| Test backup creation | Validate that backup works | `command`, `find`, `assert` |

## PCI DSS Mapping
| PCI Req | Description | Role Implementation |
|----------|--------------|--------------------|
| **10.5.3** | Protect logs and backups from modification | Set strict permissions on backup folder |
| **12.10.1** | Maintain data recovery procedures | Automated daily cron job |
| **12.10.2** | Ensure recoverability of critical systems | Test step confirms successful backup |

