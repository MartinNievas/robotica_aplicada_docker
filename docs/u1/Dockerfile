FROM dorowu/ubuntu-desktop-lxde-vnc:bionic

RUN apt-get update -q && \
    apt-get upgrade -yq && \
    apt-get install -yq wget curl git build-essential vim sudo lsb-release locales bash-completion tzdata gosu && \
    rm -rf /var/lib/apt/lists/*
RUN useradd --create-home --home-dir /home/ubuntu --shell /bin/bash --user-group --groups adm,sudo ubuntu && \
    echo ubuntu:ubuntu | chpasswd && \
    echo "ubuntu ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
RUN git clone https://github.com/Tiryoh/ros_setup_scripts_ubuntu.git /tmp/ros_setup_scripts_ubuntu && \
    gosu ubuntu /tmp/ros_setup_scripts_ubuntu/ros-melodic-desktop.sh && \
    rm -rf /var/lib/apt/lists/*
# install jupyter and configure

RUN add-apt-repository universe
RUN apt-get update && apt-get install -y \
    apache2 \
    curl \
    git \
    python3 \
    python3-pip \
    libgl1-mesa-dev \
    xorg \
    xvfb
RUN pip3 install --upgrade pip
RUN pip3 install \
    bqplot \
    ipykernel \
    ipywidgets \
    jupyterlab \
    matplotlib \
    notebook \
    pyyaml
ENV USER ubuntu
