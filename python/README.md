# Python images

This directory contains a Dockerfile for the uisautomation python image. This
image is simply the upstream Python Alpine image with updates applies, various
useful packages installed and a small set of pre-installed Python modules. These
modules are those which take a long time to install or which are common to all
of our products.

## Tags

* ``python`` is a base Python image. Tags: ``3.6-alpine``, ``alpine``, ``latest``
* ``django`` is an image with Django and common applications installed. Tags:
  ``2.0``, ``2.0-py3.6``, ``2.0-py3.6-alpine``, ``2.0-alpine``, ``alpine``,
  ``latest``

## Usage

Use like the upstream alpine image:

```Dockerfile
FROM uisautomation/python:3.6-alpine

# ...
```
