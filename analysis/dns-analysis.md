# DNS Traffic Analysis

## Objective
To investigate how DNS translates domain names into IP addresses.

## Observation
- Domain queried: `web.whatsapp.com`
- Protocol: DNS over UDP
- DNS response status: No error
- Questions: 1
- Answer records: 2
- Response time: 23.3602 ms

## DNS Response
1. CNAME: `web.whatsapp.com` resolved to `mmx-ds.cdn.whatsapp.net`.
2. A record: `mmx-ds.cdn.whatsapp.net` resolved to `57.144.139.32`.

## Conclusion
The DNS response successfully returned a CNAME record followed by an IPv4 address, demonstrating the domain name resolution process.