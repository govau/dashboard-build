[![Docker Automated build](https://img.shields.io/docker/automated/govau/dashboard-build.svg?style=plastic)](https://hub.docker.com/r/govau/dashboard-build/)
[![Docker Build Status](https://img.shields.io/docker/build/govau/dashboard-build.svg?style=plastic)](https://hub.docker.com/r/govau/dashboard-build/builds/)

# Docker image for building the dashboard

Provides a docker image with the dependencies needed for building the dashboard.

This repo is automatically built on [docker hub](https://hub.docker.com/r/govau/dashboard-build/).

### How to use it?

*Assumes you have docker running*

This image is published on [docker hub](https://hub.docker.com/r/govau/dashboard-build/). To use it:

```
docker run -it --rm -v $PWD:/workspace --workdir=/workspace govau/dashboard-build bash
```

The above command when run the first time will automatically pull the latest image from docker hub. If you run it again later, it will use the previously pulled version. To pull the latest version:

```
docker pull govau/dashboard-build
```

### How to build it locally?

*Assumes you have docker running*

1. Clone this repository:
```
git clone https://github.com/govau/dashboard-build.git
```

2. Build the image and tag it dashboard-build:
```
docker build --tag dashboard-build dashboard-build
```

3. Verify the built image:
```
docker run -it --rm dashboard-build bash
```
