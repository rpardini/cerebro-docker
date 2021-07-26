cerebro-docker-multiarch
--------------

This cerebro-docker fork publishes unofficial but multiarch images for [cerebro](https://github.com/lmenezes/cerebro) project.
Images are uploaded via Github Actions
in [rpardini/cerebro-docker](https://github.com/rpardini/cerebro-docker/pkgs/container/cerebro-docker).

### Usage

For using latest cerebro execute:

```bash
docker run -p 9000:9000 ghcr.io/rpardini/cerebro-docker:latest
```

For using a specific version run:

```bash
docker run -p 9000:9000 ghcr.io/rpardini/cerebro-docker:5a7a5ab62b749c86a5112917178e27cae5c4faa4
```

### Configuration

You can configure a custom port for cerebro by using the `CEREBRO_PORT` environment variable. This defaults to `9000`.

**Example**

```bash
docker run -e CEREBRO_PORT=8080 -p 8080:8080 ghcr.io/rpardini/cerebro-docker:latest
```

To access an elasticsearch instance running on localhost:

```bash
docker run -p 9000:9000 --network=host ghcr.io/rpardini/cerebro-docker:latest
```
