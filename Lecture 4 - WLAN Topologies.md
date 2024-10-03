# Module Focus
- This module focuses on the following topics:
	- An overview of the **active hardware** used in wireless networking
	- Brief introduction to **Antenna** classes and design
	- Network types (**BSS, ESS** and **IBSS** networks)
		- **Ad-hoc** mode vs. **Infrastructure** mode
# Types of Wireless Networks
- WLAN 802.11 (**Wi-Fi**)
- WPAN 802.15 (**Bluetooth** and **ZigBee**)
- WMAN 802.16 (**WiMAX**)
- WWAN Wireless data for mobile phones
*Some of the infrastructure elements for these are similar, some different*
*We'll focus on 802.11 gear, but occasionally mention the others*
# WLAN Hardware Components
- **WLAN** - Wireless Local Area Network
	- You'll have notices we've been pronouncing it "**y-lan**"
- **Major WLAN hardware components:**
	- **Wireless Adapters**
	- **Access Points**
	- **Wireless Routers**
	- **Antennas**
- The **next 4 slides (5-9)** illustrate some of the **physical design diversity** found in WLAN hardware components
# Wireless Adapter Examples
Image of:
- Laptop
- USB Wi-Fi adapter
- PcIE Wireless Adapter
- Ethernet to Wireless Adapter
# Access Point Examples
Image of:
- Cisco AP
- Moxa AP
- EnGenius AP
- Ubiquiti AP
# Wireless Router Examples
Image of:
- ASUS Gaming Router
- 4 Linksys Routers
# Antenna Examples
Image of:
- House Antennas
- Desktop Antenna
# STA - What does "STA" mean?
- **STA** (Station) is a term widely used in **WLAN documentation** so you need to know what it means
	- STA refers to **any device with** an **802.11-compliant radio** interface
	- When this term is used it could be referring to either an Access Point (**AP**) or a **wireless client**
# The Basic Service Set (BSS)
- A **Basic Service Set (BSS)** is the cornerstone 802.11 network topology
- A BSS has only one Access Point (AP)
- A BSS must have one or more wireless clients and their traffic must pass through the AP (no client-to-client or P2P connections)
- Optionally, the BSS's AP can be connected to a distribution system (cable-based or wireless) but this has no impact to whether or not it is considered to be a BSS
# What is an Access Point?
- A central point of connectivity for wireless clients
	- All wireless client traffic passes through the AP
- Has one or more antennas (typically two or more)
	- Built-in or connected by the cable to the AP
- Optionally (and typically) is the point of access to the cable-based network (called the distribution system)
- Is half-duplex on the AP's wireless interface side
	- Yes! Half-Duplex! Just like cable-based hubs...not surprisingly!
	- Cannot send and receive simultaneously
# SOHO Access Points
- SOHO: Small Office / Home Office
- There are two classes of SOHO APs:
1. Stand-alone AP
	1. Supports wireless communications between clients and optionally to other networks
2. Wireless Router
	1. Stand-along AP functionality plus additional functionality such as DHCP, NAT, VPN support
- In an enterprise environment, APs are often the stand-along type and rely on other infrastructure devices to provide services such as DHCP, VPN support, etc.
	- Look up! Do you think those ceiling-mounted boxes are stand-alone APs or full-on wireless routers?
		- They are stand-alone APs
# APs / Wireless Routers: Hybrid Devices
- AP and wireless router functionality falls somewhere between that of an Ethernet hub and an Ethernet switch
- Hub-like Functionality
	- Shared medium on the wireless side so only one wireless device can successfully transmit at a time
- Switch-like Functionality
	- Frame transmissions not broadcast out of all physical interfaces
		- So a frame may be sent to a specific cable-based port or it may be sent over the wireless interface
	- VLAN support allowing broadcast domain management
# Role of the Distribution System
- Access points (APs) typically serve as the portal through which data is exchanged between the wireless clients and cable-based hosts
	- An AP is rarely the target destination for wireless clients
	- Most frequently, wireless clients want to access cable-based network resources
		- e.g. the Internet, company servers
- The cable-based system to which the AP connects is referred to as the distribution system (DS)
- Do you have a DS at home?
	- Don't know
# Review
- Access Points (APs) typically serve as portals linking wireless clients to a cable-based network
- Cable-based network side is referred to as the Distribution System (DS) which for most organizations is an 802.3 Ethernet network
- Typically all of an organization's APs are connected to the DS
# AP acts as a Translation Bridge
- An AP needs an 802.11 network interface and an 802.3 network interface to translate frames that are passed back and forth between the wireless network and the Ethernet distribution system
###### So far y this seems simple - but what do you do if you can't run a cable and you need to connect an AP to your DS?
- A Wireless Distribution System (WDS) connects APs directly using a wireless link - typically in a Point-to-Point (PtP) highly directional antenna configuration referred to as a wireless backhaul
- Note that an AP interfacing to both the local wireless clients and to the other AP should have two radios set to different and non-overlapping channels to prevent throughput bottlenecks
# Multiple MAC Addresses
- What's a MAC Address?!?!
	- Unlike a cable-based hub, an AP will have two or more MAC addresses
	- Keep this in mind as we move forward!
# The Extended Service Set (ESS)
- An ESS is two or more Basic Service Sets (BSS) connected by a DS and sharing a common SSID name
- BSA coverage areas (i.e. cells) do not have to overlap to be an ESS
- It is called nomadic roaming when connectivity is lost then automatically reestablished when the client moves between non-overlapping BSA coverage areas
	- Does this sound familiar? Do we have this at the college? (Jesus fuck yes, the internet is ass sometimes)
# Another ESS Configuration
- Also an ESS because there are 2 or more BSSs connected by a DS assuming the Aps have the same SSID setting
- Overlapping coverage areas allows the client to move between BSSs without losing connectivity - called seamless roaming
# Independent Basic Service Set (IBSS)
All clients are configured with the same SSID and are using the same channel
Direct communication between wireless clients
All client stations are configured for Ad-Hoc mode (i.e. Peer-to-Peer mode (P2P))
1st client station to start up randomly generates the BSSID (MAC format) that all clients used to identify this IBSS
# Ad-Hoc vs Infrastructure Mode
- Ad-Hoc mode refers to a wireless client configuration where a wireless client communicates directly with other wireless clients
	- No AP is used
	- IBSS clients operate in ad-hoc mode
- Infrastructure mode refers to a wireless client configuration where all client communications must pass through a AP
	- No direct client to client communications
	- BSS and ESS clients operate in infrastructure mode
# Service Set Identifier (SSID)
- An SSID is the wireless network's name
- The SSID is the name the user looks for to see which wireless networks are within range

| SSID               | CH  | Signal | Security | MAC Address       |
| ------------------ | --- | ------ | -------- | ----------------- |
| Starbucks_Wireless | 9   | 78%    | WEP      | 00-1a-27-8b-cc-3a |
| Mohawk_WiFi        | 1   | 100%   | WPA-PSK  | 00-1a-bd-22-a8-ef |
| Tim_Hortons_WiFi   | 6   | 52%    | WPA-PSK  | 01-53-d2-91-fa-37 |
An Ap and a wireless client must be configured to use the same SSID in order to communicate with each other
# Basic Service Set Identifier (BSSID)
- The SSID is user-configured so two BSSs in the same area could have the same SSID
- To eliminate the possibility of a client's frame being read by the wrong AP (assuming two APs have the same SSID), frames include the BSSID as the BSS identifier
- People use SSIDs to identify the WLAN AP but wireless client devices use the BSSID
# Basic Service Area
### AP's Basic Service Area
- Physical coverage area determined by the BSS's AP configuration & environmental factors (sometimes referred to as the cell)
### BSA Shape & Size Impacted By:
- AP transmit power
- Antenna type
- Antenna gain
- Physical surroundings
- Environmental conditions
### RSSI Threshold
- Stablishes the BSA boundary
- RSSI = Received Signal Strength Indicator