# Traefik configuration

This is my very first configuration of Traefik.
### Routers

- Dashboard
- Cat app
- Whoami
- Prometheus
- Grafana
- Custom error page


### Middlewares

- Basic Auth (admin:admin)
- Rate limit
- Custom error page
- Compress

### TLS
Using Let's Encrypt with DNS challenge and Cloudflare API


---
# Configuration

## Clone the repo
```
git clone https://gitlab.com/behnambm/traefik.git
```

## Env file
Create a file named `.compose.env` in order to store Cloudflare API key(Global API Key)
```
CF_API_KEY=YOUR_KEY
CF_API_EMAIL=YOUR_EMAIL@MAIL.COM
```

**You also need to set `A` record pointing to your domain in Cloudflare. It should be a wildcard record e.g. `*.example.com`**


## Host name

In some files e.g. `docker-compose.yml`, `dynamic.yml` there might be some fields that needs to change to you'r own host name.


## Run 
```
docker compose up -d
```

**Get docker logs to check if any errors happend**

```
docker compose logs traefik
```


---


# Screenshots

### Traefik dashboard
 
### Prometheus 

### Grafana

