# Docker-C1
Hetzner Cloud VM | CX32
### Container
| Container | Ports | Hetzner Firewall |
|--|--|--|
| Traefik | 80, 443 | accept |
| Portainer | Proxy | accept |
| Portainer Agent | 9001 | block |
| WatchTower | - | block |
| Dublicati | Proxy | accept |