### 1. **Module Focus**
- **Topics Covered**: 
  - 802.11 Frame Structure
  - Medium Access
  - Distributed Coordination Function (DCF)
  - Collision Avoidance Techniques
  - Inter-frame Spacing

### 2. **Frame Structure and Size**
- **802.11 Frames vs Ethernet Frames**: 
  - 802.11 frames can be up to **2,304 bytes** compared to Ethernet frames which are **1,522 bytes**.
  - Maximum Transmission Unit (MTU) differences can cause issues, but most applications use TCP/IP, which avoids these problems.

### 3. **Frame Addressing**
- **Addressing in 802.11 Frames**:
  - 802.11 frames can contain **up to four addresses**:
    - **Transmitter Address (TA)**
    - **Receiver Address (RA)**
    - **Source Address or Final Destination Address (optional third)**
    - **Fourth address** used in AP-to-AP wireless communication.

### 4. **Medium Access and Half-Duplex Operation**
- **Medium Access**:
  - Collisions are inevitable in wireless networks.
  - **Half-Duplex Issues**: Devices either transmit, listen, or receive but cannot do multiple actions at the same time. WLAN devices rely on **CSMA/CA** (Carrier Sense Multiple Access/Collision Avoidance) to handle these limitations.

### 5. **Collision Avoidance**
- **CSMA/CA Protocol**: 
  - Minimizes collisions but cannot eliminate them.
  - Multiple procedures ensure reduced collisions, including **Physical Carrier-Sense (Clear Channel Assessment - CCA)** and **Virtual Carrier-Sense** using timers like **Network Allocation Vector (NAV)**.

### 6. **Carrier Sense Mechanisms**
- **Physical Carrier-Sense**: 
  - Radios listen to detect if the channel is free before transmission (CCA).
  - **Virtual Carrier-Sense**:
    - Uses a timer mechanism (**NAV**) to track when a station can contend for access.
    - **Duration/ID field** helps manage channel access, ensuring fairness among devices.

### 7. **Acknowledgement (ACK) Frames**
- **Frame Duration and ACKs**:
  - A station waits for an ACK frame to confirm successful frame transmission.
  - Stations calculate the time needed for ACKs and this time is reserved using the **Duration/ID field**.

### 8. **NAV Timer and Contention Phase**
- **NAV Timer**:
  - All non-transmitting stations track the transmitting station's **Duration/ID field** and set their own **NAV timers** accordingly.
  - Once the NAV timer counts down to zero, a station can contend for access to the medium.

### 9. **Contention Phase and Backoff Timers**
- **Random Backoff Timer**:
  - Stations with data to send select a random backoff value to minimize simultaneous transmissions.
  - Once the **backoff timer** reaches zero, a station transmits its frame, provided the medium is free.

### 10. **Interframe Space (IFS)**
- **IFS Types**:
  - **SIFS** (Short Interframe Space): Used for high-priority tasks like ACKs.
  - **DIFS** (Distributed Coordination Function IFS): Used for lower-priority frames.
  - **EIFS** (Extended Interframe Space): For retransmissions when frame corruption occurs.

### 11. **Contention Window and System Hierarchy**
- **Contention Window**: 
  - The contention phase repeats after each frame transmission.
  - Different frame types use varying IFS lengths, impacting transmission priority.

### 12. **Overhead and Efficiency in CSMA/CA**
- **CSMA/CA Efficiency**: 
  - The protocol uses around 50% or more of the bandwidth for control and management functions.
  - **802.11g** typically transmits at 54 Mbps but has a throughput of around **20-25 Mbps** due to overhead.

### 13. **Summary of DCF Process**
- The DCF process includes:
  - Listening for ongoing transmissions.
  - Waiting for the **NAV timer** and **DIFS** to elapse.
  - Waiting for the **backoff timer** to reach zero before transmitting.

---
