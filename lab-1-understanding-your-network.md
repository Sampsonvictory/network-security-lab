# Lab 1: Understanding Your Network

## Objective
To learn how to inspect network configuration, test connectivity,
and investigate DNS resolution using Windows Command Prompt.

## Environment
- Operating System: Windows 10
- Tools: Command Prompt
- Network: Wi-Fi

## Experiment 1: Inspecting Network Configuration

### Command
ipconfig

### Purpose
Displays the computer's network configuration, including IP
addresses, subnet masks, and default gateways.

### Observations
- The Wi-Fi adapter displayed network configuration information.
- Ethernet and other unused network adapters showed
  "Media disconnected."

### Learning Outcome
Learned how to identify network adapters and understand basic
network configuration.

## Experiment 2: Testing IPv4 Connectivity

### Command
ping 8.8.8.8

### Purpose
Tests connectivity to Google's public DNS server using IPv4.

### Results
- Packets sent: 4
- Packets received: 2
- Packet loss: 50%
- Average response time: 599 ms

### Interpretation
The destination responded, confirming that IPv4 connectivity
was possible during the test. However, the packet loss and
high response time indicated an unstable result during this
short test.

## Experiment 3: Testing Domain Connectivity

### Command
ping google.com

### Purpose
Tests connectivity to Google using its domain name.

### Results
- Packets sent: 4
- Packets received: 4
- Packet loss: 0%
- Average response time: 52 ms
- The destination resolved to an IPv6 address.

### Interpretation
All four requests received replies. IPv6 connectivity to the
destination worked successfully during this test.

## Experiment 4: Investigating DNS Resolution

### Command
nslookup google.com

### Purpose
Queries a DNS server to obtain IP address information for
the domain google.com.

### Observations
- The DNS server responded to the query.
- The server was displayed as "unknown."
- The response was labelled "Non-authoritative answer."
- Both IPv4 and IPv6 address information was returned.

### Interpretation
DNS resolution worked successfully. The "unknown" server
label does not necessarily indicate a problem. A
non-authoritative answer is a normal DNS response.

## Experiment 5: Inspecting DHCP and DNS Configuration

### Command
ipconfig /all

### Observations
- DHCP was enabled on the Wi-Fi adapter.
- A DNS Servers field containing an IP address was present.

### Interpretation
DHCP allows network configuration to be assigned
automatically. DNS servers help resolve domain names into
IP addresses.

## Key Concepts Learned
- IP addressing
- IPv4 and IPv6
- Network connectivity
- Packet loss and response time
- DNS resolution
- DHCP
- Network adapters

## Conclusion
This lab introduced basic Windows networking tools and
demonstrated how to inspect network configuration, test
connectivity, and investigate DNS resolution.

These foundational skills support further learning in
network security and cybersecurity engineering.

## Safety and Privacy
Private network addresses and identifying network details
have been omitted from this documentation.
