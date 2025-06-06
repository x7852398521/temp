# NiFi Cluster Docker Compose

This repository provides a simple Docker Compose configuration for running a three node Apache NiFi cluster on a local Windows machine. Each NiFi node joins the same cluster using ZooKeeper.

## Usage

1. Install [Docker Desktop](https://www.docker.com/products/docker-desktop/) for Windows.
2. From this directory run:

```bash
docker compose up -d
```

The NiFi UI for each node will be available on the following ports:

- Node 1: <http://localhost:8081>
- Node 2: <http://localhost:8083>
- Node 3: <http://localhost:8085>

## HTTP vs HTTPS

The provided configuration exposes NiFi over HTTP for simplicity. For development environments this may be sufficient. For production or any environment requiring encryption or authentication, configure HTTPS by supplying TLS certificates and adjusting the `NIFI_WEB_HTTPS_PORT` and related properties. Refer to the [Apache NiFi documentation](https://nifi.apache.org/docs.html) for details on securing your cluster.

