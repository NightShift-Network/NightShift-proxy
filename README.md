# NightShift Proxy

NightShift is a self-hosted web proxy with a tabbed dark-mode interface. This repository contains the generated distribution. The readable source code is maintained in [NightShift-source](https://github.com/NightShift-Network/NightShift-source).

## Run with Node.js

Requirements: Node.js and npm, plus network access for package installation and outbound Wisp connections.

```sh
git clone https://github.com/NightShift-Network/NightShift-proxy.git
cd NightShift-proxy
npm install
npm start
```

Open http://localhost:3000. To use another port, set `PORT`, for example `PORT=8080 npm start`.

## Using NightShift

Open the NightShift page in your browser, enter a website address or search term, and press Enter. Use the sidebar to open Games or quick cloaking. Proxy preferences and bookmarks are stored in that browser.

## Run with Docker Compose

```sh
git clone https://github.com/NightShift-Network/NightShift-proxy.git
cd NightShift-proxy
docker compose up -d --build
```

By default, Compose binds the app to `127.0.0.1:3005`. Open http://127.0.0.1:3005 to use it locally. For remote access, put it behind HTTPS and configure the reverse proxy to support WebSocket upgrades on `/wisp/`; service workers require HTTPS outside localhost. Restrict public access or add authentication before exposing an instance, since anyone who can reach it can use it.

## Updating

For a Node.js install, pull the latest proxy repository changes, run `npm install`, and restart NightShift. For Docker Compose, pull the changes and rebuild with `docker compose up -d --build`.

## Source code

Browse the readable code, report issues, or contribute at [NightShift-source](https://github.com/NightShift-Network/NightShift-source). The frontend in `public/` is generated from that repository. This release was built from source commit `8d734bd878219d90b893c254461cb1973bb96b45`.
