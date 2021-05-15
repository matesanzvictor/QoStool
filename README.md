# QoStool

# Overview
Tool for measuring the network quality service (QoS) based on packet trains using standard control messages. This system measures the usual parameters of quality of service: packet loss, delay, jitter, throughput and bandwidth. Two different techniques have been implemented. The first one consists in sending and receiving ICMP echo packets, while the second one in transmitting UDP packets in order to generate ICMP port unreachable messages.

# Installation.

sudo apt-get update

make

# Usage.

To run QoStool execute the following command from the terminal:

sudo ./QoStool IP

where IP is the target IP address (e.g., 192.168.1.1).

For advanced parameters, execute help to see the options:sudo ./QoStool -h

Example: ./QoStool 192.168.1.1 -l 50 -s 10 -p 1500 -i 24 --udp.

where -l is the size of the train (50 packets), -s is the speed in Mbps (10Mbps), -p is the payload size (1500bytes), -i are the bytes of the Preamble, the CRC and the interframe-gap; --udp is the protocol used. It is also possible to send ICMP packets by writting --icmp in the command.

Author: Víctor Matesanz Cotillas, 15/05/2021.

