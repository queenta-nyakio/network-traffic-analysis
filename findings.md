# Network Traffic Analysis – Findings

## 1. DNS Traffic Analysis

**Tool:** Wireshark  
**Protocol:** DNS  
**Transport Layer Protocol:** UDP

### Observation

A DNS query and its corresponding response were captured during network traffic monitoring.

The DNS query requested the IPv4 address associated with a hostname.

### DNS Response Details

- Response status: No error
- Questions: 1
- Answer records: 2
- First record: CNAME (Canonical Name)
- Second record: A (IPv4 address)
- Observed response time: 23.3602 milliseconds

### Analysis

The DNS server returned a CNAME record pointing the requested hostname to another hostname. It then returned an A record containing the IPv4 address associated with the alias.

This demonstrates how DNS uses records to resolve domain names into IP addresses.

### Conclusion

The capture demonstrated successful DNS query-and-response communication and provided practical insight into DNS resolution.




## 2. TCP Three-Way Handshake Analysis

**Tool:** Wireshark  
**Protocol:** TCP  
**OSI Layer:** Layer 4 (Transport Layer)

### Observation

TCP packets were examined using the following Wireshark display filters:

- `tcp.flags.syn == 1`
- `tcp.flags.syn == 0`
- `tcp.flags.ack == 1 && tcp.flags.syn == 0`

Packets containing SYN, SYN-ACK and ACK flags were identified.

### Analysis

TCP uses a three-way handshake to establish a connection between a client and a server.

The process involves:

1. **SYN (Synchronize):** The client initiates a connection request.
2. **SYN-ACK (Synchronize-Acknowledgment):** The server acknowledges the request and sends its own synchronization information.
3. **ACK (Acknowledgment):** The client acknowledges the server's response.

After the successful exchange, the TCP connection is established.

### Conclusion

The analysis demonstrated how Wireshark can be used to identify TCP control flags and investigate the connection establishment process.

## 3. Security and Privacy Considerations

Private network addresses, MAC addresses, interface identifiers and unnecessary browsing details have been excluded from the published report.

Screenshots are reviewed and sanitised before being shared publicly.

## 4. Evidence

- DNS query and response screenshots.
- TCP handshake packet screenshots.

