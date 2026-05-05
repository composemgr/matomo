## 👋 Welcome to matomo 🚀

Leading open-source web analytics platform

## 📋 Description

Leading open-source web analytics platform

## 🚀 Services

- **app**: docker.io/bitnami/matomo:latest

### Infrastructure Components

- **db**: Mariadb database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/matomo/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/matomo" ~/.local/srv/docker/matomo
cd ~/.local/srv/docker/matomo
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install matomo
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
DB_USER_NAME=matomo
DB_CREATE_DATABASE_NAME=matomo
APP_ADMIN_USER=administrator
APP_ADMIN_PASS=changeme_admin_password
APP_ADMIN_USER=administrator
APP_ORG_NAME=Matomo
EMAIL_SERVER_HOST=172.17.0.1
EMAIL_SERVER_PORT=587
EMAIL_SERVER_FROM_ORG=Matomo
# ... see docker-compose.yaml for more
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:59070

## 📂 Volumes

- `./volumes/data/matomo` - Data storage
- `./volumes/data/db/mariadb/matomo` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
