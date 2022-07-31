## Install docker

```bash
curl https://get.docker.com | sh
```



## Quick Deploy

```
pip install dc-cli-jawide
dc install dc
dc install nginx-proxy-manager
```

or

```bash
pip install dc-cli-jawide
dc install dc https://raw.githubusercontent.com/jawide/dc-dc/main/dc/docker-compose.yml
dc install dc https://raw.githubusercontent.com/jawide/dc-dc/main/nginx-proxy-manager/docker-compose.yml
```



## Traditional Deploy

### 1. Deploy DC

```bash
mkdir -p /root/docker/dc
cd /root/docker/dc
curl -O https://ghproxy.com/https://raw.githubusercontent.com/jawide/dc/master/dc/docker-compose.yml
docker compose up -d
```

Username: admin

Password:  password

### 2. Deploy Nginx Proxy Manager

```bash
mkdir -p /root/docker/nginx-proxy-Manager
cd /root/docker/nginx-proxy-Manager
curl -O https://ghproxy.com/https://raw.githubusercontent.com/jawide/dc/master/nginx-proxy-manager/docker-compose.yml
docker compose up -d
```

Username: admin@example.com

Password: changeme

## Configure Reverse Proxy

| name                | port |
| ------------------- | ---- |
| nginx-proxy-manager | 81   |
| dc-backend          | 5000 |
| dc-frontend         | 5001 |
| dc-admin            | 5002 |

