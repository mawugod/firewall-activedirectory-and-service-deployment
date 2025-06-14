## Phase 1: Network Foundation (5 minutes)

### Creating the Host-Only Network

**Concept**: Host-only networks create isolated virtual networks that don't connect to the physical network, perfect for lab environments.

1. **Open VirtualBox Manager**

2. **Navigate to**: `File → Tools → Network Manager`

3. **Create Network**:
   - Click **"Create"**
   - Name: `VirtualBox Host-Only Ethernet Adapter`
   - IPv4 Address: `192.168.10.1`
   - IPv4 Network Mask: `255.255.255.0` (24-bit subnet)
  
     ![image](https://github.com/user-attachments/assets/2895f07f-a322-4326-9976-7057036d8b00)


4. **Disable DHCP**: Uncheck **"Enable Server"**
   > **Why?** Our Domain Controller will handle DHCP for better integration

### Network Design Rationale

- `192.168.10.0/24` provides 254 usable addresses
- `.1` reserved for pfSense gateway
- `.10` for Domain Controller (easy to remember)
- `.20` for Web Server
- `.30` for Management PC
- `.50-100` for DHCP pool

---
