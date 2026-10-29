# Nginx Multi-Service Cluster & Reverse Proxy on Docker 🐳

A containerized load-balancing and reverse-proxy architecture built with Docker and Nginx, routing traffic across multiple containerized web nodes and static backends.

---

## 🏗️ Architecture Overview

```
                      +-------------------+
                      |   Client Request  |
                      +---------+---------+
                                |
                      +---------v---------+
                      |   Nginx Gateway   |
                      |  (Reverse Proxy)  |
                      +----+---------+----+
                           |         |
            +--------------+         +--------------+
            |                                       |
    +-------v-------+                       +-------v-------+
    | Web Node 1    |                       | Web Node 2    |
    | (Port 8001)   |                       | (Port 8002)   |
    +---------------+                       +---------------+
```

## 🚀 Key Highlights
- **Reverse Proxy Routing**: Configured Nginx virtual hosts to distribute HTTP requests across internal service networks.
- **Micro-Services Isolation**: Each web node runs independently in isolated Docker network namespaces.
- **Zero-Downtime Resilience**: Isolated service failures prevent cluster-wide interruption.
