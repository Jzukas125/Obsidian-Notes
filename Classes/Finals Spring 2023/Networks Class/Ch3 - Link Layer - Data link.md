Link layer intro - terminology - hosts and routers : nodes, communication channels that connect adjacent nodes along communication path: links -- wired, wireless, LAN

Layer 2 Packet: frame

Context - datagram transferred by different link protocols over different links

Services - Framing, link access -- encapsulate datagram into frame, adding header, trailer. 

Services (more) - flow control, error detection, error correction, half duplex

Implementation - In each and every host, implemented in network interface card 

Error detection - detection of errors caused by noise or other impairments during transmission from the transmitter to the receiver.

Parity checking - Error-correction process in network communication that ensures data transmissions between communication nodes

single bit parity -- detected single bit errors 

two-dimensional bit parity - detect and correct single bit errors 

Checksum - detect errors in transmitted segments