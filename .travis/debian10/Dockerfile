FROM debian:buster

ARG APP_UID=2000

ARG APP_GID=2000

MAINTAINER TANGO Controls team <tango@esrf.fr>

RUN apt-get update && apt-get install -y \
  apt-utils                              \
  build-essential                        \
  cmake                                  \
  curl                                   \
  git                                    \
  libcos4-dev                            \
  libomniorb4-dev                        \
  libomnithread4-dev                     \
  libzmq3-dev                            \
  lsb-release                            \
  omniidl                                \
  python2

RUN groupadd -g "$APP_GID" tango

RUN useradd -u "$APP_UID" -g "$APP_GID" -ms /bin/bash tango

ENV PKG_CONFIG_PATH=/home/tango/lib/pkgconfig

USER tango

WORKDIR /home/tango
