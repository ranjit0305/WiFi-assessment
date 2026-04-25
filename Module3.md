# WiFi Training Program – Module 3  
## Assignment Answers (PHY Layer Deep Dive)

---

## 1. 802.11 PHY Layer Standards

| Standard | Frequency | Max Speed | Key Technology |
|----------|----------|----------|----------------|
| 802.11b  | 2.4 GHz  | 11 Mbps  | DSSS |
| 802.11a  | 5 GHz    | 54 Mbps  | OFDM |
| 802.11g  | 2.4 GHz  | 54 Mbps  | OFDM |
| 802.11n  | 2.4/5 GHz| 600 Mbps | MIMO + OFDM |
| 802.11ac | 5 GHz    | ~6.9 Gbps| MU-MIMO |
| 802.11ax | 2.4/5/6 GHz | ~9.6 Gbps | OFDMA + MU-MIMO |

### Key Comparison:
- Older → DSSS/FHSS  
- Modern → OFDM/OFDMA + MIMO  
- Trend → Higher speed + better efficiency

---

## 2. DSSS vs FHSS

### DSSS (Direct Sequence Spread Spectrum)
- Spreads signal using a **chip sequence**
- More resistant to noise
- Used in 802.11b

### FHSS (Frequency Hopping Spread Spectrum)
- Rapidly switches frequencies
- Avoids interference
- Less efficient for high data rates

### Comparison

| Feature | DSSS | FHSS |
|--------|------|------|
| Speed | Higher | Lower |
| Interference | Moderate | Low |
| Complexity | Medium | High |

---

## 3. Modulation Schemes in PHY Layer

### Common Modulations

| Scheme | Bits per Symbol | Performance |
|--------|----------------|-------------|
| BPSK   | 1              | Very robust |
| QPSK   | 2              | Moderate |
| 16-QAM | 4              | Faster |
| 64-QAM | 6              | High speed |
| 256-QAM| 8              | Very high speed |

### Insight:
- Higher modulation → Higher speed  
- But → Requires better signal quality (SNR)

---

## 4. OFDM in WLAN

### What is OFDM?
Orthogonal Frequency Division Multiplexing splits data across multiple subcarriers.

### Advantages
- Reduces interference
- Improves spectral efficiency
- Handles multipath fading

### Performance Improvement
- Parallel transmission → higher throughput
- Reliable in indoor environments

---

## 5. Wi-Fi Frequency Bands

### Bands

| Band | Frequency | Features |
|------|----------|----------|
| 2.4 GHz | 2.4–2.483 GHz | Long range, more interference |
| 5 GHz   | 5.15–5.825 GHz| High speed, less interference |
| 6 GHz   | 5.925–7.125 GHz | Very high speed (Wi-Fi 6E) |

### Channels
- 2.4 GHz → 3 non-overlapping channels
- 5 GHz → Many channels
- 6 GHz → Very wide spectrum

---

## 6. Guard Interval (GI)

### What is GI?
Time gap between symbols to avoid interference (ISI)

### Types
- **Long GI** → 800 ns
- **Short GI** → 400 ns

### Impact
- Short GI → Higher efficiency (~10% gain)
- Risk → More interference if environment noisy

---

## 7. 802.11 PHY Frame Structure

### Components

1. **Preamble**
   - Synchronization
2. **Header (PLCP Header)**
   - Data rate, length
3. **Payload (PSDU)**
   - Actual data

---

## 8. OFDM vs OFDMA

| Feature | OFDM | OFDMA |
|--------|------|--------|
| Users | Single user | Multiple users |
| Efficiency | Moderate | High |
| Used in | Wi-Fi 4/5 | Wi-Fi 6 |

### 🔹 Key Idea
- OFDMA divides subcarriers among multiple users

---

## 9. MIMO vs MU-MIMO

| Feature | MIMO | MU-MIMO |
|--------|------|---------|
| Users | Single user | Multiple users |
| Streams | Multiple | Distributed |
| Efficiency | Medium | High |

### Insight
- MU-MIMO improves multi-user performance

---

## 10. PPDU, PLCP, PMD

### Definitions

- **PPDU (PLCP Protocol Data Unit)**  
  Entire PHY frame transmitted

- **PLCP (Physical Layer Convergence Protocol)**  
  Converts MAC data to PHY format

- **PMD (Physical Medium Dependent)**  
  Handles actual transmission over air

---

## 11. Types of PPDU

### Types

| Type | Standard |
|------|----------|
| Legacy PPDU | 802.11a/b/g |
| HT PPDU     | 802.11n |
| VHT PPDU    | 802.11ac |
| HE PPDU     | 802.11ax |

### Structure
- Preamble
- Header
- Data

Each generation improves:
- Efficiency
- Multi-user handling
- Speed

---

## 12. Data Rate Calculation

### Formula
Data Rate depends on:
- Channel bandwidth
- Modulation
- Coding rate
- Number of spatial streams

### General Formula:

Data Rate = (Subcarriers × Bits per symbol × Coding Rate × Streams) / Symbol Duration

### Key Factors:
- Higher bandwidth → higher speed
- More streams → higher throughput
- Better modulation → higher rate

---

# Final Summary

- PHY layer defines transmission techniques  
- OFDM/OFDMA → core of modern Wi-Fi  
- MIMO → boosts throughput  
- GI & modulation → impact performance  
- Data rate depends on multiple parameters  

---
