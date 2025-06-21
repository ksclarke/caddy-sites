## Caddy-Sites

This repository is the source control for my DigitalOcean-hosted Docker droplet (i.e., virtual server).

It has hard-coded values because I assume I’m the only one who will ever use it. However, if you find something here
that’s useful, feel free to borrow it for your own purposes.

### Getting Started

The `Caddyfile` at the root of this repo configures Caddy as a proxy server for the services running in Docker
containers. The `docker-compose.yml` file specifies which services are managed by Docker. Both files are uploaded
to the server by this repo's [GitHub Actions](./.github/workflows) whenever a new version of the repo is tagged.

There are also some systemd service files in the `services` folder. They manage the DigitalOcean Spaces (S3-compatible)
mounts and the startup/configuration of Docker Compose-controlled web services. Currently, these `*.service` files are
just stored here for safekeeping; there is no automated synchronization between this repo and the server for them.

_tl;dr: Updates are automated, but changes to the `services/*.service` files still require manual updates on the server._

### Contact

If you'd like to communicate about this repo, feel free to open a [ticket](https://github.com/ksclarke/caddy-sites/issues) or, if you're reporting a security issue, feel free to [contact me](mailto:my.security@kevinclarke.info) directly.
