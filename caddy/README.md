# Caddy Cloudflare

Web server using an **unofficial** Docker image by [IAreKyleW00t](https://github.com/IAreKyleW00t/docker-caddy-cloudflare) with built-in Cloudflare DNS module for automatic SSL certificates.

## Prerequisites

### Cloudflare

Go to your [dashboard](https://dash.cloudflare.com/profile/api-tokens) on the Cloudflare website and create a token with **DNS:Edit** permissions in the **API Tokens** section.

### Docker

Create a network for the container:

```bash
sudo docker network create caddy-cloudflare
```

Create volumes for the container:

```bash
sudo docker volume create caddy-cloudflare-data && sudo docker volume create caddy-cloudflare-config
```

## Configuration

| **Name**               | **Required** | **Default** | **Description**                                                                                                  |
| ---------------------- | ------------ | ----------- | ---------------------------------------------------------------------------------------------------------------- |
| `CLOUDFLARE_API_TOKEN` | Yes          | —           | Cloudflare API token with DNS edit permissions, used for automatic SSL certificate issuance via DNS-01 challenge |
