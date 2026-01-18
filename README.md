# Network-Security-Simulation

Overview
This project demonstrates the design and analysis of a virtualized network environment to simulate real-world cyberattacks. By engineering a topology with GNS3 and VirtualBox, I conducted network reconnaissance and a Denial of Service (DoS) attack to analyze traffic behavior and system failure points using industry-standard tools.

Technical Stack

Simulator: GNS3 

Virtualization: VirtualBox 

Network Nodes: Cisco Router (C3745), Kali Linux, VPCS 

Security Tools: Nmap (Recon), hping3 (Attack), Wireshark (Analysis) 

Simulation Phases
1. Topology Design
Built a functional network with a Cisco C3745 router as the gateway (192.168.0.1).

Configured subnets for a victim host (VPCS) and an attacker machine (Kali Linux).

2. Reconnaissance (Nmap & NBTscan)
Performed NBTscan to map the internal network's attack surface.

Executed an Nmap Stealth Scan (-sS) to identify open ports (TCP/1 to 65389) while evading full TCP handshake completion.

4. Traffic Analysis & DoS Attack
Simulated a high-volume ICMP Flood using hping3 against the victim's IP.

Transmitted over 245,000 packets in a single session, resulting in a successful Denial of Service and session timeout on the victim machine.

Captured and analyzed malicious traffic in Wireshark to correlate packet volume with system performance degradation.
