# Docker-Chrome-Node

`Dockerfile` for <https://hub.docker.com/r/reacteev/chromium-node>.

The image has:

- node
- chromium

## Getting Started

```bash
docker run -it --rm --volume "$(pwd):/app" reacteev/chromium-node:latest /bin/sh
```

## Contributing

> Tag with Git the versions of Node and Chromium, like `node-18.16.0-alpine_chromium-112.0.5615.165`.

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

## Todo

- [ ] Add GitHub Actions to push images to the Docker hub, see this documentation <https://docs.docker.com/build/ci/github-actions/update-dockerhub-desc/>.
