# 🛰️ Benedict Adjei  

**`Network Security Engineer (Routing | Switching | Wireless | Security)`**    

I’m a network security engineer passionate about building **secure, reliable, and efficient networks**.  
My projects focus on real-world networking solutions using tools like **Cisco Packet Tracer**,  
and I enjoy turning complex routing, switching, VoIP, wireless, and security concepts into simple, working designs.  

I believe in **learning by doing** — every project here reflects my growth in networking and cybersecurity.  
I hold certifications in **HCIA Datacom**, **Fortinet Certified Associate in Cybersecurity**,  
and **Fortinet Certified Fundamentals in Cybersecurity**.  

<p align="left">
   <a href="https://www.linkedin.com/in/benedict-network-sec/">
      <img alt="linkedin" title="Connect with me on LinkedIn" src="https://custom-icon-badges.demolab.com/badge/-Connect%20On%20LinkedIn-blue?style=for-the-badge&logo=person-add&logoColor=white"/>
   </a>
</p>

---

### 🧰 Skills and Tools  

   <p> a. Routing & Switching.</p>
   <p> b. Security. </p>
   <p> c. Wireless Technologies.</p>
   <p> d. VoIP Telephony.</p>

### 📂 Featured Projects  
   <p>  A.) ##📞 Cisco VoIP Telephony Lab – Day 1</p>

   <p> This project is part of my 3-Day VoIP Configuration Journey, where I build and document a working VoIP network using Cisco Packet Tracer. The goal is to demonstrate      how Voice over IP (VoIP) works, and how IP phones can be configured to communicate within the same VLAN. </p>

**🔎 What is VoIP?**

Voice over Internet Protocol (VoIP) allows voice communication to travel over IP networks instead of traditional phone lines. With VoIP, IP Phones act like computers, connecting to switches and routers to make calls.

**🛠️ Lab Topology**

Router: Cisco 2811 (configured as DHCP server + Call Manager Express)

Switch: Cisco 2960 (configured with Voice VLAN)

IP Phones: Cisco 7960 (4 phones)

Each phone is assigned an extension number:

IP Phone 1 → 1001

IP Phone 2 → 1002

IP Phone 3 → 1003

IP Phone 4 → 1004

⚙️ Configurations
**✅ On Router (2811)**

DHCP with Option 150 (for / CME)

Sub-interface Fa0/0.10 for VLAN 10 (Voice VLAN)

Telephony-service (defined extensions, auto-assign to phones)

**✅ On Switch (2960)**

Access Ports set to Voice VLAN 10 (for IP phones)

Trunk Port to Router (for inter-VLAN communication)

**📡 Protocols & Features Used**

DHCP → Assigns IPs to phones automatically

Option 150 → Directs phones to Call Manager (router IP)

VLAN 10 → Dedicated voice VLAN for call quality

CME (Call Manager Express) → Handles call setup & signaling

**📞 Results**

After completing the configuration:

Each phone received an IP via DHCP.

Phones were registered with the router.

I could dial extensions (1001–1004) between phones and establish calls successfully.

**🚀 Next Steps (Day 2 & Day 3)**

Explore call flow in more detail

Add PCs alongside phones to test data + voice VLANs

Troubleshoot call drops and QoS (Quality of Service) </p>

&nbsp;

<p> <b></b>VoIP Telephony – Dial Peering Configuration (Day 3)##</p></b> 
📌 Project Overview

This project is part of my VoIP Telephony Lab Series, built using Cisco Packet Tracer. On Day 3, I focused on Dial Peering, which enables seamless communication between two remote branches — Accra and Kumasi — using internal VoIP extensions.

Accra Branch Extensions: 1001 – 1003

Kumasi Branch Extensions: 1004 – 1006

Dial Peering allows IP Phones in one branch to call phones in another without relying on PSTN lines, reducing costs and improving scalability.

🖼️ Topology

Routers: Cisco 2811 (R1 & R2)

Switches: Cisco 3650 Multilayer Switches

IP Phones: Cisco 7960 Series

WAN Link: 10.0.0.0/30 connecting R1 ↔ R2

Routing Protocol: OSPF for branch interconnectivity

Voice VLANs:

VLAN 10 & VLAN 20 (Accra)

VLAN 30 & VLAN 40 (Kumasi)

⚙️ Configurations
🔹 R1 (Accra) Highlights
dial-peer voice 10 voip
 destination-pattern 1...
 session target ipv4:10.0.0.2

🔹 R2 (Kumasi) Highlights
dial-peer voice 10 voip
 destination-pattern 1...
 session target ipv4:10.0.0.1


Each site is configured with telephony-service for IP Phones, DHCP pools with option 150, and OSPF for routing.

🌍 Real-Life Analogy

Think of Dial Peering as building a direct road between two towns (Accra ↔ Kumasi). Without this “road,” communication would need to pass through expensive, external paths (PSTN). With Dial Peering, users can dial short internal extensions as if they are in the same office.

✅ Key Benefits

Cost Savings – Reduces dependency on PSTN lines

Scalability – Easy integration of new branches into the VoIP system

Flexibility – Internal extension dialing across remote sites

Efficiency – Faster, seamless communication between teams
