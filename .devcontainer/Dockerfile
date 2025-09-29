ARG BASE_IMAGE=lcas.lincoln.ac.uk/lcas/ros-docker-images:jammy-cuda12.2-humble-2

FROM ${BASE_IMAGE} AS base

USER root

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get install -qq -y --no-install-recommends \
    git \
    qt6-base-dev \
    libxcb-cursor0 \
    python3-pip \
    python3-rosdep

FROM base AS final
# add user ros with sudo rights if it doesn't exist

# add sudo without password
ENV DEBIAN_FRONTEND=noninteractive
ENV QT_QPA_PLATFORM=xcb

USER ros

