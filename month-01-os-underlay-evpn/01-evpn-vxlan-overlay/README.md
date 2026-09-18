# 🧪 Lab 03: EVPN-VXLAN Overlay Fabrics

## 🎯 Objectives
- Configure VXLAN Tunnel End Points (VTEPs) and VNIs via NVUE.
- Deploy BGP EVPN control plane for Type-2 (MAC/IP) and Type-5 (IP Prefix) routes.
- Validate multi-tenant Layer 2/Layer 3 overlay connectivity across the underlay.

*8-Step structure for configuring EVPN - VxLAN - it's the right one for hands-on config work*
Step 1 — Loopback and interfaces
Step 2 — Underlay BGP
Step 3 — EVPN + l2vpn-evpn AFI ⚠️ (the line that was missing on leaf02)
Step 4 — VXLAN tunnel endpoint (NVE)
Step 5 — VLAN-to-VNI mapping and access ports
Step 6 — SVIs with anycast gateway
Step 7 — L3VNI + VRF-to-EVPN route leaking
Step 8 — Data plane test