# rspi-monitoring

Raspberry Pi system monitoring using [Glances](https://github.com/nicolargo/glances) — a cross-platform monitoring tool that exposes metrics via a web UI.

## Stack

- **Glances** running in web server mode (`-w`) on port `61208`
- **Docker Compose** for container management
- **GitHub Actions** for automated redeployment on push

## Access

Once deployed, the Glances web UI is available at:

```
http://<raspberry-pi-ip>:61208
```

## Deployment

Pushes to `main` trigger a redeployment to the production runner.
Pushes to `dev` trigger a redeployment to the dev runner.

Can also be triggered manually via **Actions → Redeploy Stack → Run workflow**.

## Local start

```bash
docker compose up -d
```
