# Websocket client

Setting up a websocket client in C++ using the `socket.io` library and CMake as a preprocessor.
*(for alternatives instalation methods of the library please refer to the official repo [here](https://github.com/socketio/socket.io-client-cpp#installation-alternatives))*

Setting up a websocket client in [[C++]] using the `socket.io` library (for more information on this lib see the [[socketio-doc]])and CMake as a preprocessor. For informations on how to setup the [[Server]]

*(for alternatives installation methods of the library please refer to the official repo [here](https://github.com/socketio/socket.io-client-cpp#installation-alternatives))*

---

## Setting up the project :

The project architecture should look like this :

```
.
|-include
|-libs
| `-socket.io-client-cpp
|-CMakeLists.txt
|-main.cpp
`-tests
```

If that's the case please clone the `socket.io` repository in the `./libs` directory :

```shell

$ git clone https://github.com/socketio/socket.io-client-cpp.git

```

---

## Getting started :
First import the header files of the library :

First import the header files of the library :

```cpp
#include "libs/socket.io-client-cpp/src/sio_client.h"  
```

*(all the headers of the lib needed for using the lib are included in this one)*

Then create a socket pointer to the current socket :

```cpp
sio::socket::ptr current_socket;
```


---
# Links
Here are the links to others obsidians notes (even if the appear before )
[[Server]] [[C++]] [[socketio-doc]]