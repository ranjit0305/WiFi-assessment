# WiFi Training Program – Module 2
## Assignment Answers

---

## 1. Split-MAC Architecture

### What is Split-MAC?
Split-MAC divides MAC layer functions between:
- **Access Point (AP)** → Handles real-time operations
- **Wireless LAN Controller (WLC)** → Handles management & control

### Division of Work

| AP (Local MAC)                  | WLC (Central MAC)                  |
|--------------------------------|-----------------------------------|
| Frame transmission             | Authentication                    |
| Acknowledgement (ACK)          | Encryption policies               |
| Time-critical operations       | Roaming decisions                 |
| Beacon generation              | RF management                     |

###  How it Improves Performance
- Reduces load on AP → lightweight devices
- Centralized control → better scalability
- Faster updates → configuration done at WLC
- Efficient roaming → handled centrally

**Result:** Better performance, easier management, and scalability

---

## 2. CAPWAP Protocol & Flow

### What is CAPWAP?
**CAPWAP (Control And Provisioning of Wireless Access Points)**  
Protocol used for communication between AP and WLC.

---

### CAPWAP Flow (Step-by-Step)

1. **Discovery Phase**
   - AP finds WLC via:
     - DHCP option 43
     - DNS
     - Broadcast

2. **Join Phase**
   - AP sends join request
   - WLC authenticates AP

3. **Configuration Phase**
   - AP downloads configuration from WLC

4. **Data Transfer Phase**
   - Client traffic flows via CAPWAP tunnel

---

### Simple Flow

AP → Discover → WLC
AP → Join Request → WLC
WLC → Config → AP
AP ↔ WLC → Data Tunnel Active


---

## 3. CAPWAP in OSI Model & Tunnels

### OSI Layer
- CAPWAP works at **Layer 3 (Network Layer)** using UDP

---

### Two Tunnels in CAPWAP

| Tunnel Type     | Port | Purpose |
|----------------|------|--------|
| Control Tunnel | UDP 5246 | AP ↔ WLC control messages |
| Data Tunnel    | UDP 5247 | Client data forwarding |

---

### Purpose
- **Control Tunnel** → Management, authentication, config
- **Data Tunnel** → Carries user traffic

---

## 4. Lightweight AP vs Cloud-Based AP

| Feature              | Lightweight AP              | Cloud-Based AP            |
|----------------------|----------------------------|---------------------------|
| Controller           | Physical WLC               | Cloud controller          |
| Management           | On-premise                 | Remote (internet)         |
| Scalability          | Limited                    | Highly scalable           |
| Deployment           | Complex                    | Easy                      |
| Cost                 | Higher upfront             | Subscription-based        |

---

## 5. CAPWAP Tunnel Maintenance

CAPWAP tunnel is maintained using:

### Mechanisms
- **Keepalive Messages**
  - AP and WLC send periodic signals
- **Heartbeat**
  - Ensures connection is alive
- **Rejoin Process**
  - If connection lost → AP reconnects automatically

### Failure Handling
- If WLC unreachable → AP tries:
  - Primary → Secondary → Backup WLC

---

## 6. Sniffer Mode vs Monitor Mode

| Feature        | Sniffer Mode                          | Monitor Mode                     |
|---------------|--------------------------------------|----------------------------------|
| Purpose       | Packet capture                       | Network monitoring               |
| Traffic       | Captures specific channel            | Scans all channels               |
| Usage         | Troubleshooting                      | Security + intrusion detection   |
| Tool Example  | Wireshark                            | WIPS (Wireless IPS)              |

---

### Use Cases

**Sniffer Mode**
- Debug connectivity issues
- Analyze packets

**Monitor Mode**
- Detect rogue APs
- Detect attacks (deauth, spoofing)

---

## 7. Best AP Mode for WAN WLC Deployment

### Answer: **FlexConnect Mode**

### Why?
- Local switching of traffic
- Reduces WAN dependency
- Works even if WAN is slow

### How it Works
- Control traffic → WLC (WAN)
- Data traffic → Local network (LAN)
 Best for branch offices

---

## 8. Challenges with Autonomous APs (>50 APs)

### Problems

1. **No Central Management**
   - Each AP configured manually

2. **Scalability Issues**
   - Hard to manage large networks

3. **Roaming Problems**
   - No seamless handoff

4. **Security Risks**
   - Inconsistent policies

5. **RF Interference**
   - No centralized optimization

---

## 9. When WLC Goes Down (Lightweight AP – Local Mode)

### What Happens?

- AP loses CAPWAP connection
- Client sessions may:
  - **Disconnect** OR
  - Continue temporarily (depending on config)

---

### Behavior Details

| Scenario                  | Result                          |
|--------------------------|---------------------------------|
| Existing clients         | May stay connected briefly      |
| New clients              | Cannot authenticate             |
| Long outage              | Clients disconnected            |

---

###  Solution
- Use:
  - **Secondary WLC**
  - **High Availability (HA)**
  - **FlexConnect Mode**

---

# Final Summary

- Split-MAC = AP + WLC workload split  
- CAPWAP = AP ↔ WLC communication  
- Two tunnels → Control & Data  
- FlexConnect = best for WAN  
- Autonomous APs = not scalable  
- WLC failure impacts authentication  

---
