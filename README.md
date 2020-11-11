# drone-git

Drone plugin to clone `git` repositories.

## Build

Build the Docker image with the following commands:

```
docker build --rm -f docker/Dockerfile.linux.amd64 -t 595659439703.dkr.ecr.eu-west-1.amazonaws.com/drone-git:1.3-3 .
```

## Usage

Clone a commit:

```
docker run --rm \
  -e DRONE_REMOTE_URL=https://github.com/drone/envsubst.git \
  -e DRONE_BUILD_EVENT=push \
  -e DRONE_COMMIT_SHA=15e3f9b7e16332eee3bbdff9ef31f95d23c5da2c \
  -e DRONE_COMMIT_BRANCH=master \
  drone/git
```
