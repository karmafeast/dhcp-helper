# dhcp-helper
mini dhcp helper

e.g. in a given `docker-compose.yml`:

```dockerfile
---
services
  dhcphelper:
    build: ./dhcp-helper
    restart: unless-stopped
    network_mode: "host"
    command: -s 172.31.0.100
    cap_add:
      - NET_ADMIN
```
