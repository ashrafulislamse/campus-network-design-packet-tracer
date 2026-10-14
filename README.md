# University Campus Network Design — Cisco Packet Tracer

A complete two-campus university network simulation built in Cisco Packet Tracer: **10 department VLANs**, inter-VLAN routing (router-on-a-stick + RIP v2), per-VLAN DHCP, port security, and Web/FTP/DNS services — designed wireless-first for student and staff mobility.

> Group practical project for **Computer Communication and Network** (Bachelor of IT) — designed and implemented by **Md Ashraful Islam** and team. The full design report with configuration screenshots and testing evidence is included.

## ✨ Features

- **Two-campus topology** — Main campus (Management/HR/Finance, Library, Student Labs, Lecturers' Room, IT Department) + smaller Health & Science campus, interconnected via serial links
- **10 department VLANs** with clean /24 segmentation (plan below)
- **Inter-VLAN routing** — 802.1Q subinterfaces (router-on-a-stick) + RIP v2
- **Per-VLAN DHCP pools** served by the central router
- **Layer-2 security** — port security (MAC limits), ACLs between VLANs, DHCP snooping
- **Network services** — intranet Web server, FTP file sharing, DNS
- **Wireless-first** — access points on every floor for laptops and mobile devices
- **Verified** — ping/traceroute tests across VLANs + Packet Tracer simulation-mode walkthroughs (in the report)

## 🗺️ Network Plan (VLAN & IP addressing)

| VLAN | Department | Subnet | Gateway |
|------|------------|--------|---------|
| 10 | Management | 192.168.10.0/24 | 192.168.10.1 |
| 20 | HR | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Finance | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Computer Lab | 192.168.40.0/24 | 192.168.40.1 |
| 50 | Library | 192.168.50.0/24 | 192.168.50.1 |
| 60 | Student Labs | 192.168.60.0/24 | 192.168.60.1 |
| 70 | Lecturers' Room | 192.168.70.0/24 | 192.168.70.1 |
| 80 | IT Department (servers) | 192.168.80.0/24 | 192.168.80.1 |
| 90 | Student Lab (small campus) | 192.168.90.0/24 | 192.168.90.1 |
| 100 | Staff Offices (small campus) | 192.168.100.0/24 | 192.168.100.1 |

**Servers:** Web `192.168.80.10` · FTP `192.168.80.11` (IT VLAN 80)

## 🖥️ Devices

2× Cisco 2911 routers · 10× Catalyst 2960-24TT switches · 2× multilayer switches · 33 PCs · 4 laptops · 13 printers · Web/FTP/DNS servers · wireless access points

## 🚀 How to Use

1. Install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) (free via Cisco Networking Academy)
2. Open `campus-network-design.pkt`
3. Explore: **Logical View** → device racks → **Simulation Mode** to watch packets cross VLANs
4. Test: `ping` / `traceroute` between departments — working examples in the report

## 📚 What You'll Learn From This Repo

VLAN design & trunking · 802.1Q subinterfaces · inter-VLAN routing · RIP v2 · DHCP scopes · port security & ACLs · hierarchical campus design (core/distribution/access) · Packet Tracer simulation and testing workflow

Perfect for networking students building their first campus-scale Packet Tracer project — copy the plan, learn the config patterns, make it yours.

## 📄 Report

The complete project report (design rationale, topology diagrams, per-department IP tables, configuration screenshots, ping/traceroute test evidence) is included as `campus-network-design-report.pdf` (cover pages with personal identifiers redacted for privacy).

## 👥 Team

Group project — Bachelor of Information Technology, Semester 202409 — designed and implemented by **Md Ashraful Islam** and team.

## 📄 License

MIT — free to learn from, reuse, and build on. Attribution appreciated.
