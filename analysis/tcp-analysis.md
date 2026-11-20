# TCP Three-Way Handshake Analysis

## Objective
To examine how TCP establishes a connection between a client and a server.

## Display Filters
- `tcp.flags.syn == 1 && tcp.flags.ack == 0`
- `tcp.flags.syn == 1 && tcp.flags.ack == 1`
- `tcp.flags.ack == 1 && tcp.flags.syn == 0`

## Observations

1. SYN: The client initiated a connection.
2. SYN-ACK: The server acknowledged the request.
3. ACK: The client acknowledged the server's response.

The source and destination IP addresses and port numbers were compared to correlate the packets in the same connection.

## Conclusion
The capture demonstrated a successful TCP three-way handshake. Wireshark allowed inspection of TCP control flags and connection establishment.