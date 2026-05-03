# 🔐 WiFi Training Program – Module 6  
## Assignment Answers (Wi-Fi Security)

---

## 1. Pillars of Wi-Fi Security

###  Core Security Principles

1. **Confidentiality**
   - Prevent unauthorized access to data
   - Achieved using encryption (AES)

2. **Integrity**
   - Ensures data is not modified
   - Uses message integrity checks (MIC)

3. **Availability**
   - Ensures network is accessible when needed

4. **Authentication**
   - Verifies identity of users/devices

5. **Authorization**
   - Grants access based on permissions

---

## 2. Authentication vs Encryption

| Feature | Authentication | Encryption |
|--------|---------------|------------|
| Purpose | Verify identity | Protect data |
| When | Before access | During transmission |
| Example | Password, 802.1X | AES encryption |

### 🔹 Simple Idea
- Authentication → "Who are you?"  
- Encryption → "Hide the data"

---

## 3. WEP vs WPA vs WPA2 vs WPA3

| Feature | WEP | WPA | WPA2 | WPA3 |
|--------|----|-----|------|------|
| Security | Weak | Better | Strong | Very Strong |
| Encryption | RC4 | TKIP | AES | AES + SAE |
| Key Mgmt | Static | Dynamic | Strong | Advanced |
| Status | Obsolete | Deprecated | Widely used | Latest |

---

## 4. Why WEP is Insecure

### Reasons
- Uses weak RC4 encryption
- Static keys (no change)
- Short IV (Initialization Vector)
- Easy to crack (minutes using tools)

---

## 5. Why WPA2 was Introduced

### Problems in WPA
- TKIP still weak
- Limited security

### WPA2 Improvements
- Uses **AES encryption**
- Stronger data protection
- Mandatory for modern networks

---

## 6. Role of PMK in 4-Way Handshake

### PMK (Pairwise Master Key)
- Derived from:
  - Password (PSK) OR
  - Authentication server (802.1X)

### Role
- Used to generate session keys (PTK)
- Never directly transmitted

---

## 7. How 4-Way Handshake Ensures Authentication

### Process

1. AP sends **ANonce**
2. Client generates **SNonce**
3. Both derive **PTK**
4. Exchange MIC to verify keys

### Result
- Mutual authentication
- Secure key establishment

---

## 8. Wrong Passphrase in 4-Way Handshake

### What Happens?

- Client derives incorrect PMK
- PTK mismatch occurs
- MIC verification fails

### Result
- Handshake fails
- Connection denied

---

## 9. Problem Solved by 802.1X

### Issue
- Shared passwords (PSK) are insecure in large networks

### Solution
- Individual authentication per user

### Uses
- RADIUS server
- Enterprise security

---

## 10. How 802.1X Enhances Security

### Features

- Centralized authentication (RADIUS)
- Dynamic key generation
- Per-user access control
- Supports EAP methods

### Benefits
- Stronger security than PSK
- Scalable for enterprises
- Better access management

---

# Final Summary

- Security pillars → Confidentiality, Integrity, Authentication  
- WPA3 > WPA2 > WPA > WEP  
- 4-way handshake ensures secure key exchange  
- PMK → base for encryption keys  
- 802.1X → enterprise-level security  

---
