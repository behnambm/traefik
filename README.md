# Traefik Configuration

Welcome to my very first Traefik configuration! I've got some things that you need to manage your web traffic, including routers, middlewares, and TLS.

### Routers: Keep Your Traffic Flowing

To ensure a seamless user experience, I've set up the following routers:

- Dashboard: Manage your traffic like a pro with Traefik's user-friendly dashboard.
- Cat app: Let users access your cat app.
- Whoami: Check that your configurations are working smoothly with this useful tool.
- Prometheus: Monitor your traffic and gather key insights with this powerful tool.
- Grafana: Get a comprehensive overview of your web traffic metrics and stay ahead of the game.
- Custom error page: Keep your users engaged even when things go wrong with a custom error page.

### Middlewares: Take Your Traffic Management to the Next Level

My middlewares provide the following features to take your traffic management to the next level:

- Basic Auth (admin:admin): Keep your content secure with basic authentication.
- Rate limit: Prevent server overload by setting limits on the number of requests.
- Custom error page: Engage your users even when something goes wrong with a custom error page.
- Compress: Make your website load faster and reduce bandwidth usage.

### TLS: Secure Your Traffic

I'm using Let's Encrypt with DNS challenge and Cloudflare API to ensure your traffic is always secure.

---

# Configuration

Ready to get started? Here's what you need to do:

## Clone the Repo

Clone my repo with this command:

```bash
git clone https://gitlab.com/behnambm/traefik.git
```

## Env File

Create a file named `.compose.env` and store your Cloudflare API key (Global API Key) with the following format:

```env
CF_API_KEY=YOUR_KEY
CF_API_EMAIL=YOUR_EMAIL@MAIL.COM
```

**Don't forget to set an `A` record pointing to your domain in Cloudflare. Make sure it's a wildcard record, e.g., `*.example.com`.**

## Host Name

Some files, like `docker-compose.yml` and `dynamic.yml`, require you to change the host name to your own.

## Create acme file

```bash
touch configs/letsencrypt/acme.json

chmod 600 configs/letsencrypt/acme.json
```

## Run

Start Traefik with the following command:

```bash
docker compose up -d
```

**To check for any errors, run the following command:**

```bash
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


And that's it! Your web traffic is now under your control with Traefik. Thanks for checking out my configuration!

