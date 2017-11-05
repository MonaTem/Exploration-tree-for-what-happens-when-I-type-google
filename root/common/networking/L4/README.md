On destination machine, the L3 destination address and the machine address will match. The packets will be consumed by the machine, where the L3 module on it will reassemble them and send the resulting data above to the L4 service for further processing.


IP works together with TCP (Transmission Control Protocol) to ensure that the transmission is reliable, such that no data packet is lost, that they are in order and that there is no unreasonable delay.

In some services, TCP is replaced with UDP (Unified Datagram Packet) which does not cater reliability in transmission and just sends the packets over. For example, some VoIP systems use UDP for calls. Lost packets may not affect the call quality a lot.
