# VOIDNET | Homelab & Radio Infrastructure

Welcome to the official documentation for **VOIDNET**, a dedicated homelab environment built for enterprise network segmentation, encrypted DNS privacy, home server hosting, and digital public safety radio monitoring.

---

## 🌐 Topology Overview

```text
[ External WAN / Wi-Fi ]
           │
  [ GL.iNet Beryl AX ] ── (GL-MT3000 / Repeater Mode Bridge)
           │
  [ FortiGate 81E PoE ] ── (Core Security Edge & Routing)
           │
   [ Aruba 2530 24G ] ── (J9775A Managed Switch / VLAN Trunking)
           │
  ┌────────┴───────────────────────────┐
  │                                   │
[ HP EliteDesk 800 G3 Mini ]   [ RTL-SDR Node ]
(Win10 Ent LTSC 2021 IoT)      (RTL-SDR Blog V4 + SDRTrunk)
 ├── AdGuard Home (DoT / DoH)
 └── Core Node Services
