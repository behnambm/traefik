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
![Screenshot from 2023-02-17 23-57-25](https://user-images.githubusercontent.com/26994700/219871676-c5526478-959a-4d76-a3b8-b659c8d98f63.png)
![Screenshot from 2023-02-17 23-57-47](https://user-images.githubusercontent.com/26994700/219872189-94a67018-effe-4229-946a-618876888098.png)

### Prometheus 
![Screenshot from 2023-02-18 00-01-29](https://user-images.githubusercontent.com/26994700/219871698-7f6ec669-3b0c-4385-9601-06a4c9727c0b.png)

### Grafana
![Screenshot from 2023-02-18 00-10-15](https://user-images.githubusercontent.com/26994700/219871704-14a847be-da19-4b1e-9f6f-0df83011a1ae.png)

