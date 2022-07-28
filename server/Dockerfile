FROM ubuntu:20.04

WORKDIR /usr/is-workspace


# Install colcon
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y python3-pip git build-essential cmake libyaml-cpp-dev libboost-program-options-dev libssl-dev libwebsocketpp-dev libboost-dev
RUN pip3 install -U colcon-common-extensions

# Clone source eProsima
RUN git clone https://github.com/eProsima/Integration-Service.git src/Integration-Service --recursive
RUN git clone https://github.com/eProsima/WebSocket-SH src/WebSocket-SH
RUN git clone https://github.com/eProsima/FastDDS-SH.git src/FastDDS-SH

# Build
RUN apt-get install -y libboost-system1.71-dev
RUN colcon build --install-base /usr --merge-install