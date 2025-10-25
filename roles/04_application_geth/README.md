# role: 04_application_geth

Mục đích: Tạo user system cho geth, tạo thư mục dữ liệu/keystore, triển khai systemd unit bảo mật cho Geth.

Usage:
- Configure variables in defaults/main.yml or override in playbook/group_vars/host_vars.
- Ensure geth binary is installed (default path /usr/bin/geth) before running.

Key security considerations:
- Keystore permissions set to 0700, owned by geth.
- Systemd flags: ProtectSystem, PrivateTmp, NoNewPrivileges, CapabilityBoundingSet empty.
- Service runs as non-root system user.

Testing: see test plan in documentation or playbook README.

