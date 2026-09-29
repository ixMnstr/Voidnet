# VOIDNET | Network Hardware & Interface Infrastructure

This document details the core networking layer of **VOIDNET**, including physical connectivity, device configurations, interface mappings, and switch port assignments across the topology.

---

## 1. Physical Architecture & Cable Flow

```text
[ External Wi-Fi / WAN Source ]
              │ (Wireless Transport)
  ┌───────────┴───────────┐
  │  GL.iNet Beryl AX     │  GL-MT3000 (Bridge / Captive Portal Edge)
  └───────────┬───────────┘
              │ (WAN Port Ethernet)
  ┌───────────┴───────────┐
  │  FortiGate 81E PoE    │  Core Security Gateway & Firewall Router
  └───────────┬───────────┘
              │ (Interface Trunk Link)
  ┌───────────┴───────────┐
  │  Aruba 2530 48G       │  J9775A Managed Layer 2 Switch
  └─────┬───────────┬─────┘
        │           │
 [ HP EliteDesk ]  [ RTL-SDR Node ]
 (Server Host)     (P25 Receiver)

Network Hardware & Interfaces

## 1. GL.iNet Beryl AX (GL-MT3000)
- **Role:** Wi-Fi Repeater & WAN Transport
- **Configuration:** Captive portal bridging, passing WAN directly to the FortiGate edge.

## 2. FortiGate 81E PoE
- **Role:** Core Edge Security Gateway
- **Features:** Hardware-accelerated routing, firewall policies, and DHCP Option 6 assignment.

## 3. Aruba 2530 24G Switch (J9775A)
- **Role:** L2 Switching & VLAN Trunking
- **Uplink:** Ethernet trunk to FortiGate interface.
- **Port Allocations:**
  - `Ports 1-8`: Managed Server Node Access
  - `Ports 9-16`: General Network Access
  - `Ports 17-24`: PoE Devices / Reserved
