[![add-on registry](https://img.shields.io/badge/DDEV-Add--on_Registry-blue)](https://addons.ddev.com)
[![tests](https://github.com/d34dman/ddev-notification-server/actions/workflows/tests.yml/badge.svg?branch=main)](https://github.com/d34dman/ddev-notification-server/actions/workflows/tests.yml?query=branch%3Amain)
[![last commit](https://img.shields.io/github/last-commit/d34dman/ddev-notification-server)](https://github.com/d34dman/ddev-notification-server/commits)
[![release](https://img.shields.io/github/v/release/d34dman/ddev-notification-server)](https://github.com/d34dman/ddev-notification-server/releases/latest)

# DDEV Notification Server

## Overview

This add-on integrates Notification Server into your [DDEV](https://ddev.com/) project.

## Installation

```bash
ddev add-on get d34dman/ddev-notification-server
ddev restart
```

After installation, make sure to commit the `.ddev` directory to version control.

## Usage

| Command | Description |
| ------- | ----------- |
| `ddev describe` | View service status and used ports for Notification Server |
| `ddev logs -s notification-server` | Check Notification Server logs |

## Advanced Customization

To change the Docker image:

```bash
ddev dotenv set .ddev/.env.notification-server --notification-server-docker-image="busybox:stable"
ddev add-on get d34dman/ddev-notification-server
ddev restart
```

Make sure to commit the `.ddev/.env.notification-server` file to version control.

All customization options (use with caution):

| Variable | Flag | Default |
| -------- | ---- | ------- |
| `NOTIFICATION_SERVER_DOCKER_IMAGE` | `--notification-server-docker-image` | `busybox:stable` |

## Credits

**Contributed and maintained by [@d34dman](https://github.com/d34dman)**
