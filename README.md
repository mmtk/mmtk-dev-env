# MMTk Dependencies

This repo provides a docker file which lists the dependencies of [MMTk](https://github.com/mmtk/mmtk-core) and its bindings for [V8](https://github.com/mmtk/mmtk-v8), [OpenJDK](https://github.com/mmtk/mmtk-openjdk) and [JikesRVM](https://github.com/mmtk/mmtk-openjdk).

This docker file is based-on the official _Ubuntu-18.04_ (bionic) docker image which can be found [here](https://hub.docker.com/_/ubuntu).
As the docker is minimal, the docker file may install packages (such as `locales`) which are already included on a standard Ubuntu-18.04 installation.

Unless stated otherwise in the dockerfile, package versions are the latest installable through the `apt-get` command on _Ubuntu-18.04_.

## Software Dependencies

Currently, the MMTk team run the development and testing of MMTk and bindings on Ubuntu-18.04.

As in [Dockerfile](https://github.com/mmtk/mmtk-docker/blob/main/Dockerfile), setting up the dependencies can be done through these steps:

1. Install the required packages: [Dockerfile#17](https://github.com/mmtk/mmtk-docker/blob/main/Dockerfile#L17),
2. Install `rustup` and add it to `PATH`: [Dockerfile#20-21](https://github.com/mmtk/mmtk-docker/blob/main/Dockerfile#L20-L21),
3. Install our currently used nightly Rust toolchain using `rustup`: [Dockerfile#25](https://github.com/mmtk/mmtk-docker/blob/main/Dockerfile#L25),
4. Add the `i686-unknown-linux-gnu` target to the Rust toolchain: [Dockerfile#26](https://github.com/mmtk/mmtk-docker/blob/main/Dockerfile#L26)

__NOTE:__ We successfully tried the same procedure on Ubuntu-20.04, but Ubuntu-18.04 is still the version we use daily.

## Supported Hardware

We use an _AMD Ryzen 9 3900X_ Machine with 32GB RAM, running _Ubuntu 18.04.5 LTS (GNU/Linux 5.4.0-47-generic x86_64)_, for MMTk development.
