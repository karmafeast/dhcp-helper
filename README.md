# dhcp-helper

dhcp helper / relay agent

e.g. in a given `docker-compose.yml` (the command is specifying the target of the relay):

```dockerfile
---
services
  dhcphelper:
    image: karmaterminal/dhcp-helper:latest
    restart: unless-stopped
    network_mode: "host"
    command: -s x.x.x.x
    cap_add:
      - NET_ADMIN
```
