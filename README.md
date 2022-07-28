# poc-eprosima-is

### Criteria
* Security connection between **robot client** and **back-end server**
* Simple configuration (remap IDL, topic, request-response service, server)
* Low-latency
* Bandwidth (serialized message, binary)
* Scalability
* Performance (CPU-bound, IO-bound)

# Dependencies
#### Docker
* [Docker Ubuntu](https://https://docs.docker.com/engine/install/ubuntu/)

#### Integration Service Core
* [YAML-cpp](https://github.com/jbeder/yaml-cpp): A *YAML* parser and emiter for C++.
* [Boost program options](https://github.com/boostorg/program_options): Library that allows obtaining name-value pairs from the config file.

  These libraries can be installed using your Linux distribution package manager with the following command:
```bash
sudo apt-get install -y libyaml-cpp-dev libboost-program-options-dev
```
#### WebSocket System Handle

* [OpenSSL](https://www.openssl.org/): Toolkit for the Transport Layer Security (TLS) and Secure Sockets Layer (SSL) protocols.
* [WebSocket++](https://github.com/zaphoyd/websocketpp): *WebSocket* Protocol C++ library implementation.

  These libraries can be installed using your Linux distribution package manager with the following command:

  ```
  sudo apt-get install -y libssl-dev libwebsocketpp-dev
  ```
# Quick Start
### Server
1. Build dockerfile
    ```bash
    docker build -t poc-eprosima-is/server server/.
    ```
2. 