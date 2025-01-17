## Caddy-Sites

This repo contains:
* A root `Caddyfile` that controls how different services are routed on my Digital Ocean server. This is deployed to the server via this repo's GitHub Action (on creation of a tag in this repo).
* A `server-configs` directory, which contains a clean `Caddyfile` with the `admin` interface enabled and a `docker-compose.yml` file that runs the Caddy Docker container on the server (stored here in case the server ever needs to be recreated from scratch).
* A GitHub Action that publishes the latest tagged version of the root `Caddyfile` to the Digital Ocean server's `admin` endpoint.

Access to the Caddy `admin` endpoint is controlled by the `docker-compose.yml` file, which only opens the port to the local server. The GitHub Action in this repo shells into the Digital Ocean server to run commands locally.

### Contact

If you'd like to communicate about this repo, feel free to open a [ticket](https://github.com/ksclarke/caddy-sites/issues) or, if you're reporting a security issue, feel free to [contact me](mailto:my.security@kevinclarke.info) directly.