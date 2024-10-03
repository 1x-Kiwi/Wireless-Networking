# Module Focus
- This module focuses on the following topics:
	- Wireless vs. wired networks
	- The Electromagnetic (EM) spectrum
	- EM wave fundamentals
	- Measuring EM waves
# Comparing Wires & Wireless Networks
- In a wired network devices must be connected by a wire to communicate
- A wired network is a ***bounded*** medium: data must travel over whatever path the wire or cable takes between the devices
- Shortcomings: lack of mobility, need for compatible connectors, etc.
- Wireless network devices do not need to be tethered to a cable
- More convenient and mobile
- Many different devices can easily connect to a wireless network, such as Laptops, Smartphones and many wireless control devices such as thermostats.
- Wireless data must travel through free space
	- Good: fewer constraints
	- Bad: lacks the protection of a wire
- To make this work, wireless engineering focuses on two things:
	- A common standard
	- Wireless coverage must exist in the area where devices are expected
- In a *wired link* an electrical signal is applied at one end and carried to the other end
- For transmission in *free space* a different method is required:
	- The sender sends an alternating current into a short piece of wire (the **antenna**)
	- This sets up a moving electric and magnetic field that emanates from the antenna (**propagates**) as travelling waves
- Note: The signal must keep changing, or alternating, by cycling up and down
	- This keeps the electric and magnetic fields cycling and pushing ever outward
	- Do these signals travel outwards forever?
		- No
# The Electromagnetic Spectrum
## What are Electromagnetic Waves?
- We've already mentioned that we transmit a wireless signal by setting up a moving electric and magnet field that emanates from the antenna as travelling waves
- We call these waves **Electromagnetic waves**
	- Characterized by **energy oscillations** of combined **electric** and **magnetic fields** which travel at light speed in a vacuum
- Wavelengths range from **extremely short gamma waves** to **very long radio waves** and all together they are referred to as the **electromagnetic spectrum**
- For ease of reference, the **electromagnetic spectrum** is **subdivided** into sections referred to as **wavebands**
	- **Radio spectrum** (i.e. **radio waveband**) is one of these wavebands
	- **802.11 WLANs** operate **within** the **radio spectrum**

# Industrial, Scientific & Medical (ISM) Bands
- There are **3 ISM bands**:
	- 1. **951 MHz ISM Band**
		- 902 MHz - 928 MHz
		- **Not used** by IEEE 802.11 devices
	- 2. **2.4 GHz ISM Band**
		- 2.4000 GHz - 2.4835 GHz
			- **83.5 MHz** of bandwidth
		- **Used** by **802.11 Prime/b/g/n/ac/ax** devices
	- 3. **5.8 GHz ISM Band**
		- 5.725 GHz - 5.875 GHz
		- **Not Used** by IEEE 802.11 devices
			- 802.11a/n/ac (etc.) use the U-NII bands instead
# Wave Terminology
- **Wireless networks** use the **radio waveband** to carry signals
- To understand how wireless networks work you must know some **basic terminology** related to **electromagnetic waves** including the following
	- **Frequency**
	- **Wavelength**
	- **Amplitude**
# What is Frequency?
- **Frequency** is the number of **wave cycles** passing by a specific point in a **second**
- **Unit of measurement** is the **hertz**
	- Abbreviation: **Hz**  
- If **one wave cycle** is completed **per second** the the frequency is **1 Hz**

| 1 Kilohertz (kHz) | 1,000 Hz             |
| ----------------- | -------------------- |
| 1 Megahertz (MHz) | 1,000,000 Hz         |
| 1 Gigahertz (GHz) | 1,000,000,000 Hz     |
| 1 Terahertz (THz) | 1,000,000,000,000 Hz |

---

# Text Book Section Summary

---

### **1. Comparing Wired and Wireless Networks**
- **Wired Networks**: These networks rely on physical connections (cables or wires) between devices, ensuring a stable and bounded transmission medium. Wired networks are predictable because they have strict standards (like IEEE 802.3 for Ethernet) that control how data is transmitted.
- **Wireless Networks**: In contrast, wireless networks transmit data over radio frequencies (RF), which introduces challenges such as variable signal quality due to environmental factors like interference. Wireless networks rely on the IEEE 802.11 standard for wireless local area networks (WLANs). The biggest advantage of wireless networks is mobility, allowing users to move freely while maintaining connectivity.

---

### **2. Understanding Basic Wireless Theory**

#### **How RF Signals Work**
- **Electromagnetic Waves**: Wireless signals travel as electromagnetic waves, which consist of oscillating electric and magnetic fields that propagate through space. These fields are always at right angles to each other, and the waves expand outward from the transmitter in all directions.
- **Signal Propagation**: RF signals can be thought of as expanding spheres, with the energy radiating from the antenna in all directions. At the receiving end, antennas pick up these waves and convert them back into electrical signals for the receiving device.

#### **Frequency**
- **Definition**: Frequency refers to the number of complete cycles (oscillations) a signal makes in one second. It is measured in hertz (Hz). For example, a signal that oscillates 4 times in a second has a frequency of 4 Hz.
- **Wireless Frequency Bands**:
   - The document focuses on two main bands for wireless communication: 
     - **2.4 GHz band**: Ranges from 2.400 GHz to 2.4835 GHz. It is divided into channels, with each channel spaced 5 MHz apart. There are 14 channels in this band.
     - **5 GHz band**: Composed of four sub-bands from 5.150 GHz to 5.825 GHz. Each band is used for different purposes (Wi-Fi, radar, etc.). The 5 GHz band typically has less interference but shorter range than 2.4 GHz.

#### **Phase**
- **Phase Definition**: The phase of a signal refers to its position in time relative to the start of a cycle. A signal that starts at the same time as another is “in phase,” while one that is delayed is “out of phase.”
- **Phase Importance**: When two signals are in phase, they can add together constructively, amplifying the signal. When they are out of phase, especially by 180 degrees, they can cancel each other out, weakening the overall signal. This becomes critical in environments with multiple wireless devices.

#### **Wavelength**
- **Wavelength vs Frequency**: Wavelength is the physical distance a wave travels during one complete cycle. As frequency increases, wavelength decreases. For example, a 2.4 GHz signal has a wavelength of approximately 4.92 inches, while a 5 GHz signal has a shorter wavelength of about 2.36 inches.
- **Practical Use**: Understanding wavelength helps in the design of antennas, which must be compatible with the wavelength of the signals they transmit or receive.

---

### **3. Understanding RF Power and Decibels (dB)**
- **Power Levels**: RF signal strength is critical for ensuring successful wireless communication. Power levels are measured in milliwatts (mW), but comparing power levels is often done using decibels (dB).
   - **dBm**: A measure of power relative to 1 milliwatt. For example, 0 dBm is equal to 1 mW, and 20 dBm equals 100 mW.
- **Free Space Path Loss**: As RF signals travel through space, they lose power. This natural attenuation is known as free space path loss and can be mitigated by increasing the power at the transmitter or using directional antennas to focus the signal.

---

### **4. Carrying Data Over an RF Signal**

#### **Modulation Techniques**
Modulation is the method of encoding data onto a carrier RF signal, allowing it to be transmitted wirelessly.

- **Frequency-Hopping Spread Spectrum (FHSS)**:
   - FHSS works by rapidly switching the carrier among many frequency channels. This helps avoid interference, as the signal spends only a brief time on each frequency.
   - While FHSS improves reliability, it supports lower data rates and is less efficient than other methods.
  
- **Direct-Sequence Spread Spectrum (DSSS)**:
   - DSSS spreads data across a wide frequency band, using a mathematical sequence to encode the data. It is less vulnerable to interference and more efficient than FHSS.
   - **Data Rates**: DSSS supports data rates of 1 Mbps, 2 Mbps, 5.5 Mbps, and 11 Mbps, depending on the modulation technique used.

- **Orthogonal Frequency-Division Multiplexing (OFDM)**:
   - OFDM is used in modern wireless networks because it supports higher data rates (up to 54 Mbps or more). It works by splitting the signal into multiple sub-carriers, which transmit data in parallel. This makes OFDM highly efficient in environments with interference or multipath distortion (signals bouncing off objects).

#### **Modulation Schemes**
- **BPSK, QPSK, and QAM**:
   - Different modulation schemes are used to encode data onto the carrier signal.
     - **BPSK (Binary Phase-Shift Keying)**: Encodes data by shifting the phase of the signal by 180 degrees. It is simple but supports low data rates.
     - **QPSK (Quadrature Phase-Shift Keying)**: A more efficient modulation, QPSK shifts the signal phase by 90 degrees and can transmit two bits of data per symbol.
     - **QAM (Quadrature Amplitude Modulation)**: Combines both amplitude and phase shifts to encode more data per signal. 16-QAM and 64-QAM are used in wireless networks for higher data rates.

---

### **5. Wireless Channels and Interference**

#### **Channel Allocation**
- **2.4 GHz Band Channels**: In this band, 14 channels are spaced 5 MHz apart. However, each channel requires a bandwidth of 22 MHz, meaning that adjacent channels overlap and can cause interference.
  - **Non-overlapping Channels**: Only channels 1, 6, and 11 are non-overlapping in the 2.4 GHz band. These are typically used in networks to minimize interference.

- **5 GHz Band Channels**: The 5 GHz band offers many more channels (up to 23 non-overlapping channels), making it ideal for high-density environments where multiple devices need to connect without causing interference.

#### **Types of Interference**
- **Co-Channel Interference (CCI)**: Occurs when multiple access points (APs) use the same channel. Devices sharing a channel must compete for airtime, which reduces overall network performance.
- **Adjacent Channel Interference (ACI)**: Happens when overlapping channels are used, leading to signal interference that degrades performance.
- **Non-802.11 Interference**: Devices like Bluetooth, microwave ovens, and cordless phones can cause significant interference in the 2.4 GHz band.

---

### **6. Understanding Antennas**

#### **Antenna Characteristics**
- **Radiation Patterns**: An antenna’s radiation pattern shows how it disperses RF energy. Patterns can be:
  - **Omnidirectional**: Antennas emit signals equally in all directions, forming a circular coverage area. These are useful in environments where devices are spread out in all directions.
  - **Directional**: Focus energy in a specific direction, forming a narrower, more concentrated beam. These are ideal for long-distance communication or covering specific areas.

- **Gain**: Measured in decibels (dBi), antenna gain represents the increase in signal strength. Higher-gain antennas focus RF energy in a particular direction, improving the signal range.

#### **Antenna Types**
- **Omnidirectional Antennas**: Commonly used in indoor environments like offices, these antennas provide 360-degree coverage, making them suitable for access points (APs) that need to serve devices in multiple directions.
- **Directional Antennas**: Used in point-to-point links or to cover a specific area, these antennas focus energy into a narrow beam, providing stronger signals over longer distances.

#### **Polarization**
- **Antenna Polarization**: Refers to the orientation of the electric field emitted by the antenna. It can be either horizontal or vertical. For optimal performance, the transmitting and receiving antennas should have the same polarization.

---

### **Conclusion**
The content from pages 8–24 covers the foundational concepts of wireless networks, including RF signal properties, modulation techniques, interference management, and antenna characteristics. These are critical for understanding how wireless networks are designed, implemented, and optimized.