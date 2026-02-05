---
created: 2025-11-14
title: How to run forgejo with podman?
tags:
aliases:
links:
  - "[[forgejo]]"
  - "[[podman]]"
---
## Container Configuration

1. Create persistent storage directories

```bash
mkdir -p /var/containers/forgejo/{config,data,log}
chown $USER:$USER /var/containers/forgejo/{config,data,log}
chmod 755 /var/containers/forgejo/{config,data,log}
```

2. [[Podman Quadlets|Quadlet]] file at `~/.config/containers/systemd/forgejo.container`

```ini
[Unit]
Description=Forgejo Git Forge
After=network-online.target
Wants=network-online.target

[Container]
ContainerName=forgejo
Image=codeberg.org/forgejo/forgejo:12-rootless
AutoUpdate=registry
Volume=/var/containers/forgejo/data:/var/lib/gitea:Z
Volume=/var/containers/forgejo/config:/etc/gitea:Z
Volume=/var/containers/forgejo/log:/var/lib/gitea/data/log:Z
ShmSize=256m
PublishPort=4000:3000
PublishPort=2022:2022

[Service]
Restart=always

[Install]
WantedBy=multi-user.target default.target
```
## Reverse Proxy

```nginx
server {
    server_name code.example.com;
    location / {
        proxy_pass http://127.0.0.1:4000/;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
    }
    client_max_body_size 100M;
}
```

## SSH Configuration

4. Open firewall port 2022
5. Set `SSH_CLIENT_PORT = 2022` in `/var/containers/forgejo/config/app.ini`
6. Add to `~/.ssh/config` on your machine:
```ssh
Host code.example.com
    Port 2022
```

## Deployment

```bash
systemctl --user daemon-reload
systemctl --user start forgejo
```