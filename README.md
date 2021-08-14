# Docker-Chrome-Node

## Build the image

> Tag with Git the versions of Node and Chromium, like `node-14.17.5-alpine_chromium-81.0.4044.113`.

```bash
docker build \
  --tag reacteev/chromium-node:latest \
  --tag reacteev/chromium-node:$(git describe --tag) \
  .
```
