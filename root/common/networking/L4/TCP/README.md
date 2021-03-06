# TCP connection flow

- Client chooses an initial sequence number (ISN) and sends the packet to the server with the SYN bit set to indicate it is setting the ISN
- Server receives SYN and if it's in an agreeable mood:
   - Server chooses its own initial sequence number
   - Server sets SYN to indicate it is choosing its ISN
   - Server copies the (client ISN +1) to its ACK field and adds the ACK flag to indicate it is acknowledging receipt of the first packet
- Client acknowledges the connection by sending a packet:
   - Increases its own sequence number
   - Increases the receiver acknowledgment number
   - Sets ACK field
- Data is transferred as follows:
   - As one side sends N data bytes, it increases its SEQ by that number
   - When the other side acknowledges receipt of that packet (or a string of packets), it sends an ACK packet with the ACK value equal to the last received sequence from the other
- To close the connection:
   - The closer sends a FIN packet
   - The other sides ACKs the FIN packet and sends its own FIN
   - The closer acknowledges the other side's FIN with an ACK
