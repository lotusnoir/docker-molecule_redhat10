# Docker Image with redhat10 base image

This repo was created in order to test ansible roles with molecule.

## Build it locally

  docker build -t redhat10img .
  docker run -d   --name redhat10con --privileged --cgroupns=host -v /sys/fs/cgroup:/sys/fs/cgroup:rw   --tmpfs /run   --tmpfs /run/lock   --tmpfs /tmp   redhat10img
  docker exec -it redhat10con bash

## Use it from dockerhub

    https://hub.docker.com/repository/docker/lotusnoir/ansible_molecule_test_images:redhat10
