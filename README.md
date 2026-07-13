## Caddy-Sites

This repository contains the configuration files for my DigitalOcean droplet.

### Getting Started

The repository root contains two primary configuration files:

- `Caddyfile` configures Caddy as a reverse proxy for services running in Docker containers.
- `docker-compose.yml` defines the Docker services managed on the droplet.

When a repository version is tagged, a GitHub Actions workflow deploys both files to the server. See [`.github/workflows`](./.github/workflows) for the deployment workflow.

### Host Configuration

The following files are stored in this repository for reference and backup. They are not automatically deployed or synchronized to the droplet.

| Repository path | Purpose | Path on Droplet |
| --- | --- | --- |
| `services/*.service` | These are systemd units for DigitalOcean Spaces mounts and Docker Compose service startup/order | `/etc/systemd/system/` |
| `etc/fuse.conf` | This is a FUSE configuration, which includes the settings required by the rclone mounts | `/etc/fuse.conf` |
| `config/rclone/rclone.conf` | This is an rclone configuration for use with the mounted DigitalOcean Spaces buckets | `$HOME/.config/rclone/rclone.conf` |

### Contact

To ask a question or report a non-security issue, open an [issue](https://github.com/ksclarke/caddy-sites/issues).

For security issues, please [contact me directly](mailto:my.security@kevinclarke.info).
