# WiFi Training Program – Module 5  
## Assignment Answers (Wi-Fi 6, 6E, 7 & Roaming)

---

## 1. Key Features of Wi-Fi 6, 6E and 7 (vs Wi-Fi 5)

### Wi-Fi 5 (802.11ac) – Baseline
- Works only in **5 GHz**
- Supports **MU-MIMO (downlink only)**
- Uses **256-QAM**
- Good speed but poor efficiency in dense networks

---

### Wi-Fi 6 (802.11ax)

**Main Focus → Efficiency + Capacity**

- Works in **2.4 GHz + 5 GHz**
- **OFDMA** → Multi-user transmission
- **MU-MIMO (uplink + downlink)**
- **1024-QAM** → Higher throughput
- **BSS Coloring** → Reduces interference
- **TWT (Target Wake Time)** → Power saving

---

### Wi-Fi 6E

**Extension of Wi-Fi 6 with new spectrum**

- Adds **6 GHz band**
- No legacy device interference
- Wider channels available (80/160 MHz clean spectrum)
- Lower latency

---

### Wi-Fi 7 (802.11be)

**Main Focus → Extreme performance**

- **320 MHz channels**
- **4096-QAM**
- **Multi-Link Operation (MLO)**
- Enhanced OFDMA
- Deterministic low latency

---

### Quick Comparison

| Feature | Wi-Fi 5 | Wi-Fi 6 | Wi-Fi 6E | Wi-Fi 7 |
|--------|--------|--------|---------|--------|
| Bands | 5 GHz | 2.4/5 | 2.4/5/6 | 2.4/5/6 |
| QAM | 256 | 1024 | 1024 | 4096 |
| Efficiency | Medium | High | Very High | Extreme |
| Latency | Medium | Low | Lower | Ultra-low |

---

## 2. Role of OFDMA in Wi-Fi 6

### Concept
OFDMA divides a channel into **Resource Units (RUs)** so multiple users can transmit at the same time.

###  Why Important
- Traditional Wi-Fi → One user per time slot  
- OFDMA → Many users simultaneously  

### Benefits
- Lower latency
- Better spectrum utilization
- Ideal for dense environments (classrooms, stadiums)

---

## 3. Target Wake Time (TWT)

### Concept
- AP schedules when a device should wake up and transmit/receive

### Benefits (especially IoT)
- Battery saving (devices sleep most of the time)
- Reduces channel contention
- Improves overall efficiency

---

## 4. Significance of 6 GHz Band (Wi-Fi 6E)

### Key Advantages

- Large contiguous spectrum (~1200 MHz)
- No legacy devices → cleaner environment
- More non-overlapping channels
- Supports high bandwidth (160 MHz)

###  Result
- Higher throughput
- Lower interference
- Reduced latency

---

## 5. Wi-Fi 6 vs Wi-Fi 6E

| Feature | Wi-Fi 6 | Wi-Fi 6E |
|--------|--------|----------|
| Bands | 2.4 + 5 GHz | 2.4 + 5 + 6 GHz |
| Interference | Medium | Very Low |
| Channels | Limited | Plenty |
| Latency | Low | Lower |
| Range | Better | Slightly lower (6 GHz) |

---

## 6. Innovations in Wi-Fi 7 (802.11be)

### Major Improvements

- **320 MHz channels** → Double bandwidth of Wi-Fi 6
- **4096-QAM** → More data per symbol
- **Multi-Link Operation (MLO)** → Parallel links
- **Multi-RU allocation** → Better OFDMA efficiency
- Deterministic latency for real-time apps

### Outcome
- Extremely high throughput
- Ultra-low latency
- Improved reliability

---

## 7. Multi-Link Operation (MLO)

### Concept
- Device uses **multiple bands/channels simultaneously** (e.g., 5 GHz + 6 GHz)

### Types
- Link aggregation
- Link switching
- Load balancing

### Impact
- Increased throughput
- Reduced latency
- Better reliability (failover support)

---

## 8. 802.11k and 802.11v (Roaming Optimization)

### 802.11k (Neighbor Reports)
- AP provides list of nearby APs
- Helps client make faster roaming decision

### 802.11v (Network Assisted Roaming)
- AP suggests best AP to client
- Improves roaming efficiency

---

## 9. 802.11r (Fast BSS Transition)

### Problem Solved
Normal roaming takes time due to re-authentication

### Solution
- Pre-authentication with target AP
- Fast key exchange

### Benefit
- Seamless roaming
- Critical for:
  - VoIP
  - Video calls
  - Real-time applications

---

## 10. How 802.11k/v/r Work Together

### Combined Flow

1. **802.11k** → Client gets nearby AP list  
2. **802.11v** → AP recommends best AP  
3. **802.11r** → Fast authentication & handoff  

### Result
- Smooth roaming
- Minimal packet loss
- Low latency transition

---

# Final Summary

- Wi-Fi 6 → Efficiency (OFDMA, MU-MIMO, TWT)  
- Wi-Fi 6E → Clean 6 GHz spectrum  
- Wi-Fi 7 → Ultra performance (MLO, 4096-QAM)  
- TWT → Power saving for IoT  
- 802.11k/v/r → Seamless enterprise roaming  

---
