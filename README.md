# Docker image for BeagleBone Black Node applications

Provides a x86-64 Vagrant box with `docker` and `qemu` provisioned to enable building an ARM architecture docker image with Node support, intended to be ran on a a [BeagleBone Black](http://beagleboard.org/black).  Includes an updated device tree compiler (dtc) with symbol (`-@`) support, needed when using [bonescript](https://github.com/jadonk/bonescript).

Currently based off the [mazzolino/armhf-debian](https://registry.hub.docker.com/u/mazzolino/armhf-debian/) docker image. Later I may create the image from scratch following these [instructions](
https://olimex.wordpress.com/2014/07/21/how-to-create-bare-minimum-debian-wheezy-rootfs-from-scratch/).

## Build and push image

    vagrant up
    vagrant ssh
    docker build . -t strictlybusiness/beaglebone-black-node
    docker push strictlybusiness/beaglebone-black-node
