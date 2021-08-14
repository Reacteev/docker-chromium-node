# Docker-Chrome-Node

## Getting Started

```bash
docker run -it --rm --volume "$(pwd):/app" reacteev/chromium-node:latest /bin/sh
```

## Contributing

> Tag with Git the versions of Node and Chromium, like `node-14.17.5-alpine_chromium-81.0.4044.113`.

### Build the image

```bash
docker build \
  --tag reacteev/chromium-node:latest \
  --tag reacteev/chromium-node:$(git describe --tag) \
  .
```

### Publish the image

```bash
docker login
docker push reacteev/chromium-node:latest
docker push reacteev/chromium-node:$(git describe --tag)
```
