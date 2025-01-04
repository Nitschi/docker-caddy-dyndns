# Caddy Dynamic DNS

Docker-based setup to automatically update DNS records to reflect the current IP of a server.
Useful for homeservers, where IPs regularly change.

# Usage
- `cp .env_template .env`
- Insert correct values in `.env` (For Netcup see https://helpcenter.netcup.com/en/wiki/general/our-api)
- `docker compose build --pull`
- `docker compose up -d`
- Check output with `docker logs --follow dyndns`

# Adapt to other providers
- Fork this repo
- Pick a provider from [dns_providers](https://caddyserver.com/docs/modules/dynamic_dns#dns_provider)
- Adapt Dockerfile to install the correct provider
- Adapt Caddyfile to provide the specific login data required
- Optional: Rename the environment variables in .env/.env_template, docker-compose.yml and the usage in the Caddyfile
