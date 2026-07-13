## Caddy-Sites

This repository contains the configuration files for my DigitalOcean droplet.

### Getting Started

The repository root contains two primary configuration files:

- `Caddyfile` configures Caddy as a reverse proxy for services running in Docker containers.
- `docker-compose.yml` defines the Docker services managed on the droplet.

When a repository version is tagged, GitHub Actions deploy both files to the server. See [`.github/workflows`](./.github/workflows) for the deployment workflow.

The `services/` directory contains systemd unit files. These manage the DigitalOcean Spaces (S3-compatible) mounts and control startup ordering for Docker Compose services. These files are currently stored here for reference and backup only; changes to them are not automatically deployed to the droplet.

Additional host-level configuration files are stored in the following locations:

- `etc/fuse.conf` corresponds to `/etc/fuse.conf` on the droplet.
- `config/rclone/rclone.conf` corresponds to `$HOME/.config/rclone/rclone.conf` on the droplet.

### Contact

To ask a question or report a non-security issue, open an [issue](https://github.com/ksclarke/caddy-sites/issues).

For security issues, please [contact me directly](mailto:my.security@kevinclarke.info).
