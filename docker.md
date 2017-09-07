---
title: [draft] Naming docker images
---

// vim: set syntax=asciidoc:
[[image_naming]]
= Image Naming
:data-uri:
:homepage https://github.com/projectatomic/container-best-practices:

This section describes the image naming standards for Docker images.

Docker URLs are similar to GitHub repository names. Their structure is:

  REGISTRY:PORT/USER/REPO:TAG

The implicit default registry is `docker.io`. This means that relative URLs, such as `redhat/rhel` resolve to `docker.io/redhat/rhel`. The "registry" and "repository" elements must be present in the names of images. "Port", "user", and "tag" are not always required, and are not always present.

Here is an example showing search results for a query targeting Fedora images:

  $ sudo docker search fedora
  INDEX       NAME                                             DESCRIPTION                                     STARS     OFFICIAL   AUTOMATED
  docker.io   docker.io/fedora                                 Official Fedora 21 base image and semi-off...   172       [OK]
  docker.io   docker.io/fedora/apache                                                                          30                   [OK]
  docker.io   docker.io/fedora/couchdb                                                                         30                   [OK]
  docker.io   docker.io/fedora/mariadb                                                                         22                   [OK]
  docker.io   docker.io/fedora/ssh                                                                             19                   [OK]

Here we see a search that shows an image name in the REGISTRY/USER/REPO format in the NAME column:

  $ sudo docker search zdover23
  INDEX       NAME                               DESCRIPTION   STARS     OFFICIAL   AUTOMATED
  docker.io   docker.io/zdover23/fed20publican                 0

## Links

[image_naming](https://github.com/projectatomic/container-best-practices/blob/master/deliver/image_naming.adoc)
