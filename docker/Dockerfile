FROM ubuntu:jammy

RUN apt-get update && \
  DEBIAN_FRONTEND='noninteractive' \
  DEBCONF_NONINTERACTIVE_SEEN='true' \
  apt-get install --yes \
    gfortran \
    build-essential \
    git \
    automake \
    autoconf 

RUN useradd \
  --create-home \
  mineos_user 

USER mineos_user

WORKDIR /home/mineos_user

RUN git clone 'https://github.com/geodynamics/mineos';cd mineos; ./configure; make F77='gfortran -fallow-argument-mismatch';

ENV PATH="/home/mineos_user/mineos:${PATH}"
