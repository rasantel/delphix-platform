#
# Copyright 2018 Delphix
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

FROM ubuntu:bionic-20180426

MAINTAINER Prakash Surya <prakash.surya@delphix.com>

ENV DEBIAN_FRONTEND noninteractive
ENV HOME /root

WORKDIR /root

RUN \
  apt-get update && \
  apt-get install -y software-properties-common && \
  apt-add-repository -y ppa:ansible/ansible && \
  apt-get update && \
  apt-get install -y \
      curl \
      debhelper \
      devscripts \
      dpkg-dev \
      jq \
      make \
      shellcheck \
      wget && \
  rm -rf /var/lib/apt/lists/*

RUN wget -nv -O /usr/local/bin/shfmt \
  https://github.com/mvdan/sh/releases/download/v2.4.0/shfmt_v2.4.0_linux_amd64 && \
  chmod +x /usr/local/bin/shfmt
