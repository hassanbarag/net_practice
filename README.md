*This project has been created as part of the 42 curriculum by hassamoh.*

# NetPractice

## Description

NetPractice is a networking project from the 42 curriculum. It introduces the fundamentals of IPv4 networking through practical exercises in which small simulated networks must be configured so that their devices can communicate.

The project contains **10 levels**. Each level provides a network diagram with one or more connectivity goals. To solve a level, the learner adjusts the available network settings, checks the result, and investigates the logs when communication fails.

The objective is to understand how IP addressing and routing work together, not simply to make a configuration pass.

## Instructions

### 1. Launch the training interface

1. Download the NetPractice archive from the project page.
2. Extract the archive into a directory of your choice.
3. Open a terminal in the extracted directory.
4. Run the supplied script:

   ```bash
   ./run.sh
   ```

If the script does not work, start a local web server manually from the extracted directory:

```bash
python3 -m http.server 49242
```

Then open [http://localhost:49242](http://localhost:49242) in your browser.

### Concepts

- **Client IP:** Client IP addresses must not overlap with other client IP addresses.
- **Switch:** A switch connects clients in the same subnet.
- **Router:** A router connects different subnets.
- **Routing Table:** Routes are configured using source and destination IP addresses with CIDR notation, such as `0.0.0.0/0`.
- **Private IP Addresses:** Private IP addresses are not directly accessible from the internet.

Private IP ranges:

- `10.0.0.0` – `10.255.255.255`
- `172.16.0.0` – `172.31.255.255`
- `192.168.0.0` – `192.168.255.255`

**Loopback IP range — do not set as a local network IP:**

- `127.0.0.1` – `127.255.255.254`

### Steps to Solve a Problem

1. Check the CIDR notation or subnet mask.
2. Check the specific client IP address that is assigned.
3. Calculate the available IP range in the subnet.
4. Configure the routing table according to the problem's goals.

### CIDR Sheet Table

| Address | Total Addresses | Usable Hosts | Netmask |
|---|---:|---:|---|
| `/30` | 4 | 2 | `255.255.255.252` |
| `/29` | 8 | 6 | `255.255.255.248` |
| `/28` | 16 | 14 | `255.255.255.240` |
| `/27` | 32 | 30 | `255.255.255.224` |
| `/26` | 64 | 62 | `255.255.255.192` |
| `/25` | 128 | 126 | `255.255.255.128` |
| `/24` | 256 | 254 | `255.255.255.0` |
| `/18` | 16,384 | 16,382 | `255.255.192.0` |
| `/16` | 65,536 | 65,534 | `255.255.0.0` |


## Resources

**NetPractice project instructions:** Documentation provided with the 42 project.
- **Networking tutorial — YouTube:** https://www.youtube.com/watch?v=BWZ-MHIhqjM
- **Classless Inter-Domain Routing (CIDR):** https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing
- **CIDR Calculator:** https://cidr.xyz/
- **Broadcast Address:** https://en.wikipedia.org/wiki/Broadcast_address
- **RFC 791 — Internet Protocol:** https://www.rfc-editor.org/rfc/rfc791
- **Cisco Networking Resources:** https://www.cisco.com/

The main concepts studied during this project include:

- TCP/IP and IPv4 addressing.
- Subnet masks and CIDR notation.
- Network IDs, broadcast addresses, and usable host ranges.
- Default gateways.
- Routers, switches, and network interfaces.
- Routing tables and default routes.
- Public and private IP addresses.
- Packet forwarding and return routes.
- Network connectivity troubleshooting.

### Use of Artificial Intelligence

Artificial intelligence tools, including ChatGPT, were used as learning and documentation support during this project.

AI assistance was used to:

- Explain IPv4 addressing, subnet masks, CIDR notation, network IDs, broadcast addresses, and usable host ranges.
- Clarify the roles of routers, switches, default gateways, and routing tables.
- Interpret NetPractice diagnostic logs and explain possible causes of connectivity problems.
- Support understanding of packet forwarding and routing in both directions.
- Help organize and write this README in accordance with the project requirements.

AI was used to support learning and documentation. Network configurations were tested in the NetPractice training interface, and the concepts were reviewed to improve understanding of the reasoning behind each configuration.

