# Automation docker images

[![CircleCI](https://circleci.com/gh/uisautomation/dockerimages.svg?style=svg)](https://circleci.com/gh/uisautomation/dockerimages)

This repository contains configuration to build the [UIS automation docker
images](https://hub.docker.com/r/uisautomation/). The images are built nightly
via CircleCI and pushed to Docker hub.

## Images

The following image types are built. See the README files in each image's
directory for more details.

* [python](python/README.md)

## Configuration

The [CircleCI configuration](.circleci/config.yml) iterates over the image types
and builds the docker images in each directly. Different image types may have
different versions built. If the job is running on ``master``, the images are
also pushed to Docker hub.

The CircleCI project must be set up with the Docker hub username and password in
the ``DOCKER_USER`` and ``DOCKER_PASS`` environment variables. For the
uisautomation Docker hub account see the [shared documentation
repo](https://github.com/uisautomation/docs) for these credentials.
