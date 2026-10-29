# Docker Nginx Reverse Proxy Setup

Nginx reverse proxy routing traffic across internal web nodes using Docker containers.

## Overview

- An Nginx container acts as the entry point, distributing incoming requests.
- Internal web services run on isolated container ports.
- Configured with custom Nginx virtual hosts.
