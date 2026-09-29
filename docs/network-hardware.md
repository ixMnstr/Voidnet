```markdown
# Network Hardware & Interfaces

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
