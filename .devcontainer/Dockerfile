ARG ELIXIR_VERSION=1.18.2
ARG OTP_VERSION=27.2.1
ARG DEBIAN_VERSION=bookworm-20250113-slim

ARG BUILDER_IMAGE="hexpm/elixir:${ELIXIR_VERSION}-erlang-${OTP_VERSION}-debian-${DEBIAN_VERSION}"

FROM ${BUILDER_IMAGE} AS builder

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -qq && \
    apt-get install -qq -y \
    curl \
    git \
    dirmngr \
    gpg \
    gawk \
    unzip \
    build-essential \
    autoconf \
    libssl-dev \
    libncurses5-dev \
    m4 \
    libssh-dev \
    inotify-tools

WORKDIR /app