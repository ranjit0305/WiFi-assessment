# 📡 WiFi Training Program – Module 4  
## Assignment Answers (MAC Layer Deep Dive)

---

## 1. MAC Layer Significance & OSI Position

### Position in OSI Model
- MAC layer is part of **Data Link Layer (Layer 2)**

###  Role of MAC Layer
- Controls how devices access the wireless medium
- Handles:
  - Frame transmission
  - Addressing (MAC addresses)
  - Error detection
  - Retransmission

### Significance
- Ensures **efficient sharing of wireless medium**
- Prevents collisions
- Maintains communication reliability

---

## 2. 802.11 MAC Frame Format

### Main Fields

| Field | Purpose |
|------|--------|
| Frame Control | Defines type (data/control/management) |
| Duration | Time for medium reservation |
| Address 1 | Receiver |
| Address 2 | Transmitter |
| Address 3 | Destination |
| Sequence Control | Frame ordering |
| Address 4 | Used in special cases |
| Payload | Actual data |
| FCS | Error detection |

---

## 3. MAC Layer Functionalities

### Management Plane
- Scanning (finding networks)
- Authentication
- Association
- Roaming

### Control Plane
- RTS/CTS
- ACK
- Medium reservation

### Data Plane
- Frame transmission
- Retransmission
- Fragmentation

---

## 4. Scanning Process

### Types

#### 1. Passive Scanning
- AP sends **beacon frames**
- Client listens

#### 2. Active Scanning
- Client sends **probe request**
- AP replies with **probe response**

### Comparison

| Feature | Passive | Active |
|--------|--------|--------|
| Speed | Slow | Fast |
| Traffic | Less | More |
| Power | Low | Higher |

---

## 5. Client Association Process

### Steps

1. **Scanning**
2. **Authentication**
3. **Association Request**
4. **Association Response**
5. **IP Address Assignment (DHCP)**

### Result
Client becomes part of the network

---

## 6. EAPOL 4-Way Handshake

### Purpose
- Establish secure encryption keys

### Steps

1. AP → Client: ANonce  
2. Client → AP: SNonce + MIC  
3. AP → Client: GTK  
4. Client → AP: Confirmation  

---

### Keys Derived

| Key | Purpose |
|-----|--------|
| PMK | Master key |
| PTK | Session key |
| GTK | Broadcast key |

---

## 7. Power Saving Mechanisms

### Purpose
Reduce battery usage

### Types

1. **Legacy Power Save**
   - Client sleeps
   - AP buffers data

2. **U-APSD (Unscheduled APSD)**
   - Client requests data when needed

3. **TWT (Target Wake Time)**
   - Scheduled wake/sleep cycles (Wi-Fi 6)

---

## 8. Medium Access Control Methods

### CSMA/CA (Main Method)
- Listen before transmit
- Avoid collisions

### RTS/CTS
- Reduces hidden node problem

### Backoff Algorithm
- Random delay before retransmission

---

## 9. Block ACK Mechanism

### What is Block ACK?
- Acknowledges multiple frames at once

### Advantages
- Reduces overhead
- Improves throughput
- Efficient for high-speed Wi-Fi

---

## 10. A-MSDU vs A-MPDU

### A-MSDU
- Multiple MSDUs inside one frame
- Single header
- Less overhead but error-prone

---

### A-MPDU
- Multiple MPDUs aggregated
- Each has its own header
- More reliable

---

### Comparison

| Feature | A-MSDU | A-MPDU |
|--------|--------|--------|
| Efficiency | High | Moderate |
| Reliability | Low | High |
| Error Handling | Poor | Good |

---

### A-MSDU in A-MPDU
- Combines both techniques
- Used in modern Wi-Fi for **maximum efficiency + reliability**

---

# Final Summary

- MAC layer = controls communication in Layer 2  
- Frames define communication structure  
- CSMA/CA avoids collisions  
- EAPOL ensures security  
- Aggregation improves performance  

---
