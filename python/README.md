# Python images

This directory contains a Dockerfile for the uisautomation python image. This
image is simply the upstream Python Alpine image with updates applies, various
useful packages installed and a small set of pre-installed Python modules. These
modules are those which take a long time to install or which are common to all
of our products.

## Tags

* ``python:3-6-alpine``, ``alpine``, ``latest`` - base Python image
* ``python:3-6-django-alpine``, ``django-alpine``, ``django`` - Python image
    with Django and common Django applications installed

## Usage

Use like the upstream alpine image:

```Dockerfile
FROM uisautomation/python:3.6-alpine

# ...
```
