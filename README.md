# SBA Umbrel App Store

A community app store for [Umbrel](https://umbrel.com) by Shop Bitcoin
Australia. Shows up in umbrelOS as **"SBA"**.

## Add this store to your Umbrel

1. On your umbrelOS home screen, open the **App Store**.
2. Click the **⋯** (three-dots) menu (top right) → **Community App Stores**.
3. Paste `https://github.com/bayanimills/sba-umbrel-store` and click **Add**.

The **SBA** store then appears; open it and install any app from it.

## Apps

### BlockClock Connect (`sba-blockclock`)

Point a Coinkite **BLOCKCLOCK** at the data you care about: multi-exchange
Bitcoin price, network & on-chain stats, your own node, weather, and more, all
previewed with their real backlight colour, with optional AI/agent control.

- App source & issues: **[github.com/bayanimills/blockclock-connect](https://github.com/bayanimills/blockclock-connect)**
- Image: `ghcr.io/bayanimills/blockclock-connect`

## Store structure

```
umbrel-app-store.yml        # store id ("sba") + name ("SBA")
sba-blockclock/
  umbrel-app.yml            # app listing/manifest (points at the app repo)
  docker-compose.yml        # app services (app_proxy + web, references the app image)
  icon.svg
  gallery/                  # app-store screenshots referenced by umbrel-app.yml
```

This repo holds only the store + app **manifests**. The app's **source code**
lives in its own repo, [blockclock-connect](https://github.com/bayanimills/blockclock-connect),
which builds and publishes the image to GHCR.

## Contributing

App bugs and feature/feed requests belong in the
[app repo's issues](https://github.com/bayanimills/blockclock-connect/issues);
see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE) © 2026 Bayani Mills.

---
<sub><i>Vires in numeris.</i></sub>
