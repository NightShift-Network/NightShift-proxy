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

## Run with Docker Compose

```sh
git clone https://github.com/NightShift-Network/NightShift-proxy.git
cd NightShift-proxy
docker compose up -d --build
```

By default, Compose binds the app to `127.0.0.1:3005`. For remote access, put it behind HTTPS and configure the reverse proxy to support WebSocket upgrades on `/wisp/`; service workers require HTTPS outside localhost.

## Source code

Browse the readable code, report issues, or contribute at [NightShift-source](https://github.com/NightShift-Network/NightShift-source). The frontend in `public/` is generated from that repository. This release was built from source commit `2bf3f00803207087ca0bc746b07cee6832dc0a71`.
