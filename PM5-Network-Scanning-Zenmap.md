PM4 — Active Host Discovery & Network Topology Mapping (Nmap & Zenmap)

Lab Environment: VirtualBox Internal NAT Network (10.0.0.0/24 Private Subnet)

Tools Used: iproute2 (ip a), Nmap v7.991, Zenmap GUI

Objective

Identify the local Kali Linux network interface and subnet scope, execute an active host discovery ping sweep (nmap -sn) inside Zenmap, interpret network topology symbology using the Topology Legend, and export the network topology map as a PDF artifact for SOC asset inventory documentation.

Step 1: Local Network Interface & Subnet Verification (ip a)

Command:

ip a


Screenshot:

<img width="1920" height="892" alt="nmap 1" src="https://github.com/user-attachments/assets/6f61c82b-fccb-46bb-b283-22dd270649ce" />

Output:

[nmap 1 results.txt](https://github.com/user-attachments/files/34818107/nmap.1.results.txt)

                                                                                                                                                                                                                                             
┌──(junaid㉿junaidbloch)-[~]
└─$ ip a         
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute 
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 08:00:27:4e:29:59 brd ff:ff:ff:ff:ff:ff
    inet 10.0.0.2/24 brd 10.0.0.255 scope global noprefixroute eth0
       valid_lft forever preferred_lft forever
    inet6 fe80::c73c:7180:b9b7:85d6/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever

Details & Analysis:

Active Interface (eth0): Assigned private NAT Network IP 10.0.0.2 with a /24 CIDR subnet mask (255.255.255.0), establishing a 256-host scan boundary (10.0.0.0/24).

Virtual NIC Identification: MAC address prefix 08:00:27 confirms an Oracle VirtualBox virtual Ethernet adapter.

Step 2: Active Ping Scan & Live Host Discovery (Zenmap)

Target: 10.0.0.2/24

Profile: Ping scan

Command:

nmap -sn 10.0.0.2/24


Screenshot:

<img width="1920" height="892" alt="nmap ping scan 2" src="https://github.com/user-attachments/assets/b1c69039-49db-4807-8dc5-ff6650ac55b6" />

Output:

[nmap ping scan results.txt](https://github.com/user-attachments/files/34818140/nmap.ping.scan.results.txt)
Starting Nmap 7.991 ( https://nmap.org ) at 2026-11-13 03:00 -0800
Nmap scan report for 10.0.0.1
Host is up (0.0058s latency).
MAC Address: 52:54:00:12:35:00 (QEMU virtual NIC)
Nmap scan report for 10.0.0.2
Host is up.
Nmap done: 256 IP addresses (2 hosts up) scanned in 3.20 seconds


Details & Analysis:
Starting Nmap 7.991 ( https://nmap.org ) at 2026-11-13 03:00 -0800
Nmap scan report for 10.0.0.1
Host is up (0.0058s latency).
MAC Address: 52:54:00:12:35:00 (QEMU virtual NIC)
Nmap scan report for 10.0.0.2
Host is up.
Nmap done: 256 IP addresses (2 hosts up) scanned in 3.20 seconds

Discovered Live Hosts (2 out of 256 IPs scanned in 3.20s):

10.0.0.1: VirtualBox NAT Network default gateway/router (MAC: 52:54:00:12:35:00, QEMU virtual NIC, 0.0058s latency).

10.0.0.2: Local Kali Linux analysis machine.

Stealth & Speed (-sn): Disables port scanning and performs pure host discovery (ARP requests on the local subnet), identifying live nodes rapidly without generating noisy port-scan traffic.

Step 3: Network Topology Visualization, Legend & PDF Export

Action Performed:

Switched to the Topology tab inside Zenmap, reviewed the Topology Legend to interpret node and traceroute indicators, and exported the topology graph via Save Graphic into a PDF document.

Screenshot:

<img width="1920" height="892" alt="nmap legend view" src="https://github.com/user-attachments/assets/7a5570b9-715d-46d7-8346-584ebe0cf804" />

Exported Topology Graph (PDF):

[ping scan graphic.pdf](https://github.com/user-attachments/files/34818195/ping.scan.graphic.pdf)

Details & Analysis:

Host Exposure Color Coding: As shown in the Topology Legend, nodes scanned without port enumeration (-sn) appear as unfilled white circles, whereas port-scanned hosts are color-coded by risk: Green (< 3 open ports), Yellow (3 to 6 open ports), and Red (> 6 open ports).

Connection & Device Mapping: Line thickness represents round-trip latency (blue for primary path, orange for alternate path), and specialized icons distinguish routers, switches, firewalls, and filtered hosts.

SOC Analyst Security Takeaways

Attacker Perspective: Once inside a local subnet, adversaries run fast ARP/ICMP discovery sweeps (nmap -sn) to map gateways and active endpoints for lateral movement while minimizing IDS alerts.

Blue Team Defense: SOC analysts monitor EDR and network IDS (Snort/Suricata) telemetry for sequential ARP requests or abnormal ICMP echo bursts originating from non-administrative workstations, and enforce VLAN segmentation to limit subnet visibility.
