cmake_minimum_required(VERSION 3.10)
project(testNAT)

set(CMAKE_CXX_STANDARD 11)

include_directories(NAT_UDP/common)
include_directories(NAT_UDP/linux_client)
include_directories(NAT_UDP/server)
include_directories(UDP_NAT_p2p/Client)
include_directories(UDP_NAT_p2p/Client/x64)
include_directories(UDP_NAT_p2p/Client/x64/Debug)
include_directories(UDP_NAT_p2p/Server)
include_directories(UDP_NAT_p2p/Server/x64)
include_directories(UDP_NAT_p2p/Server/x64/Debug)
include_directories(UdpHoleServer)

add_executable(testNAT
        NAT_UDP/common/protocol.h
        NAT_UDP/common/sock.h
        NAT_UDP/linux_client/unix_client.cpp
        NAT_UDP/linux_client/unix_client.h
        NAT_UDP/linux_client/unix_client_message_parser.h
        NAT_UDP/server/server.cpp
        NAT_UDP/server/server.h
        NAT_UDP/server/server_message_parser.h
        UDP_NAT_p2p/Client/x64/Debug/Client.pch
        UDP_NAT_p2p/Client/Client.cpp
        UDP_NAT_p2p/Client/client_define.h
        UDP_NAT_p2p/Client/stdafx.cpp
        UDP_NAT_p2p/Client/stdafx.h
        UDP_NAT_p2p/Client/targetver.h
        UDP_NAT_p2p/Server/x64/Debug/Server.pch
        UDP_NAT_p2p/Server/class_client_function.cpp
        UDP_NAT_p2p/Server/define.h
        UDP_NAT_p2p/Server/Server.cpp
        UDP_NAT_p2p/Server/stdafx.cpp
        UDP_NAT_p2p/Server/stdafx.h
        UDP_NAT_p2p/Server/targetver.h
        UdpHoleServer/nat-type/CServerCheckNAT.cpp
        UdpHoleServer/udp-nat-traversal/udpHoleClient.cpp
        UdpHoleServer/udp-nat-traversal/udpHoleClient_for_windows.cpp
        UdpHoleServer/udp-nat-traversal/udpHoleServer.cpp
        UdpHoleServer/HoleServer.cpp
        UdpHoleServer/NetApiDefine.cpp
        UdpHoleServer/NetApiDefine.h
        UdpHoleServer/SocketBase.h
        UdpHoleServer/SocketUDP.cpp
        UdpHoleServer/SocketUDP.h
        UdpHoleServer/ThreadSyncUtil.cpp
        UdpHoleServer/ThreadSyncUtil.h
        UdpHoleServer/UtilMakePack.cpp
        UdpHoleServer/UtilMakePack.h)
