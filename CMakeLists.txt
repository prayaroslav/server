cmake_minimum_required(VERSION 3.10)
project(server)

set(CMAKE_C_STANDARD 99)

add_executable(server.o udp/server.c my_server.h packet/packet.h packet/packet.c ID/ID.c ID/ID.h error/Error.c error/Error.h log/log.h log/log.c)

add_executable(server_slave.o udp/server_slave.c my_server.h packet/packet.h packet/packet.c error/Error.c error/Error.h log/log.h log/log.c)

##############


project(client)

set(CMAKE_C_STANDARD 99)

add_executable(client.o udp/client.c packet/packet.c ID/ID.c error/Error.c error/Error.h log/log.h log/log.c)

##############


project(client_tcp)

set(CMAKE_C_STANDARD 99)

add_executable(client_tcp.o tcp/client_tcp.c packet/packet.c ID/ID.c error/Error.c error/Error.h log/log.h log/log.c ID/ID_TCP.c)

##############

project(server_tcp)

set(CMAKE_C_STANDARD 99)

add_executable(server_tcp.o tcp/server_tcp.c my_server.h packet/packet.h packet/packet.c ID/ID.c ID/ID.h error/Error.c error/Error.h log/log.h log/log.c ID/ID_TCP.c)

add_executable(server_slave_tcp.o tcp/server_slave_tcp.c my_server.h packet/packet.h packet/packet.c error/Error.c error/Error.h log/log.h log/log.c ID/ID_TCP.c)
