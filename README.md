# Hirschbach Business Case — Fly.io Deployment

## Prerequisites
- [Fly CLI](https://fly.io/docs/flyctl/install/) installed
- Fly.io account (`fly auth login`)

## Deploy

```bash
# From this directory:

# 1. Create the app (first time only)
fly apps create hirschbach-business-case

# 2. Deploy
fly deploy
```

## Notes
- The page is password-protected. Access code: `HBXZOOM`
- Served via nginx on Alpine Linux (minimal image)
- Auto-stops when idle to save costs, auto-starts on request
- HTTPS enforced automatically by Fly.io
- Your app will be live at: `https://hirschbach-business-case.fly.dev`

## Customizing the app name
Edit `fly.toml` and change the `app` value to your preferred name. Then run:
```bash
fly apps create your-app-name
fly deploy
```
Your URL will be `https://your-app-name.fly.dev`.
