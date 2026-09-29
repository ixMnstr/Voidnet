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
