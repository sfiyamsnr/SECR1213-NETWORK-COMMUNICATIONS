# SECR1213-NETWORK-COMMUNICATIONS

# 🚀 Network Communications (SECR1213-02) - Learning Portfolio & Project Reflection

Welcome to my learning portfolio for the **Network Communications (SECR1213)** course at Universiti Teknologi Malaysia. This repository showcases my individual laboratory findings, practical packet analysis experiments, network topologies, and our comprehensive final network design architecture.

---

## 📑 Overall Course Reflection

The SECR1213 Network Communications course has been a profound journey through the core layers of the TCP/IP and OSI protocol stacks. Transitioning from absolute conceptual abstractions to physically tracking live hex payloads and calculating strict bit boundaries completely transformed my engineering perspective.

Key personal and technical takeaways include:
* **The Layered Protocol Framework:** Understanding how encapsulated data transitions downward from application payloads (like HTTP and DNS) into segments, packets, and frames made me appreciate the intricate engineering that keeps the global internet functional and secure.
* **Logical vs. Physical Network Design:** Learning that a successful network deployment is more than just connecting devices; it requires meticulous physical scale planning, budget optimizations, structural safety considerations, and dynamic traffic segregation.
* **Collaborative Network Orchestration:** Working within our group (Y-Link) taught me how crucial collaborative planning is when managing extensive infrastructure models. Cross-verifying IP allocations, testing connectivity iteratively, and analyzing operational bottlenecks mirror the workflows of real-world Network Operations Centers (NOC).

---

## 🛠️ Laboratory Exercise Reflection

### 🔹 [Lab 1: Packet Analysis at Application Layer using Wireshark]
* **Concepts Focused:** Packet sniffing architecture (`pcap` library), Application Layer communication, HTTP request/response parsing, DNS query/response mechanics, and local client network configurations (`ipconfig/all`).
* **Implementation Details:** Utilized Wireshark to isolate packet flows, inspecting standard protocol behaviors. Analyzed structure variants such as Type A DNS query payloads, local DNS mapping discrepancies (e.g., verifying local servers versus external query targets), and standard HTTP message structures.
* **Reflection:** Capturing live data packets stripped away the mystery of web interactions. Seeing how a standard browser request converts into physical text strings and mapping DNS questions directly to single-answer resource records (RRs) solidified my practical debugging mindset.

### 🔹 [Lab 2: Packet Tracer Simulation – TCP and UDP Communications]
* **Concepts Focused:** Transport Layer protocols (TCP vs. UDP), connection orchestration states (`ESTABLISHED`), multiplexing, and standard application-to-port mapping rules.
* **Implementation Details:** Evaluated standard network application traffic (HTTP, FTP, DNS, SMTP, and POP3) across multiple server types via Packet Tracer. Run deep diagnostics via `netstat` to trace active transport sessions, analyzing open port mechanics (e.g., standard Server Port 21 for persistent FTP control sessions).
* **Reflection:** This lab clearly demystified why certain applications rely on specific transport behaviors. Tracking how an FTP server stays in an `ESTABLISHED` state while awaiting explicit client instructions, versus the stateless burst interactions of UDP-bound DNS queries, gave me an intuitive grasp of network performance balancing.

### 🔹 [Lab 3: Routing Protocols]
* **Concepts Focused:** Network Layer topologies, Variable Length Subnet Masking (VLSM), static and dynamic routing configurations, Routing Information Protocol (RIP), and end-to-end connectivity diagnosis (`ping`, gateway validation).
* **Implementation Details:** Structured routing table configurations for a multi-router network layout (`JERUNG`, `SHARK`, and `TIBURON`) targeting a baseline network address block of `172.18.110.0/23`. Computed usable host requirements ranging from 20 to 60 hosts per subnetwork and solved complex missing-route communication failures.
* **Reflection:** Subnetting manually and programming routing tables forced me to treat IP addresses as strict structural pathways. Successfully diagnosing an isolated subnetwork block like `192.168.1.0/24` and learning how to correct gateways to establish complete multi-node ping success was an empowering experience in technical trouble-shooting.

### 🔹 [Lab 4 Plus: Exploration of ARP and Switch Table Communications]
* **Concepts Focused:** Data Link Layer mechanics, Address Resolution Protocol (ARP) table caches, Switch MAC Address Tables (`show mac-address-table`), and dynamic frame mapping workflows.
* **Implementation Details:** Monitored address binding operations using a multi-switch topology (`SWA`, `SWB`, `SWC`) connected via distinct routers (`RTA`, `RTB`). Logged how devices broadcast and store target hardware addresses natively, and mapped how switches dynamically register interface bindings.
* **Reflection:** This exercise resolved a common point of confusion regarding network devices. Differentiating how routers leverage ARP to bridge logical IPs to physical hardware, while switches maintain distinct MAC-to-port maps to perform hardware-level frame forwarding without altering packet headers, provided a crucial foundational block.

---

## 🏢 Final Group Project Reflection: "Y-Link Network Design"

Our group project involved building a highly secure, scalable, and optimized network infrastructure plan for the Faculty of Computing's new block (Block N28B).

### 📋 Task 1 & Task 2: Structural Floor Plans & Requirement Analysis
* **Concepts Covered:** Physical network architecture layouts, architectural scale tracking, technical and operational feasibility modeling, security parameters, and data compliance standards (GDPR/Personal Data Management).
* **Core Contribution:** I drove the structural layout plan for the Ground Floor, putting forward strategic cost-saving layouts to place academic labs on shared floors to minimize backhaul drops. I also spearheaded the comprehensive security analysis framework, ensuring that physical access controls, firewalls, and network perimeters met strict operational feasibility metrics.
* **Reflection:** Designing the floor layouts *before* allocating devices emphasized the realities of network planning. Factoring in operational growth criteria (like planning for a 15% institutional expansion) taught me that a solid network layout must remain flexible enough to handle future physical changes seamlessly.

### 🔌 Task 3 & Task 4: Device Procurement, Budgeting & Physical Connections
* **Concepts Covered:** Hardware assessment criteria, budget allocation matrices, structured cabling schemas, and network management selection.
* **Core Contribution:** Researched, benchmarked, and selected optimal enterprise-tier Server systems and Core Router hardware configurations to manage internal traffic safely. Collaborated with Dayang to calculate structural connection paths, estimate drop numbers, and manage cable layout boundaries for the ground floor zone.
* **Reflection:** Balancing raw hardware throughput against actual budgetary bounds was an eye-opening business scenario. We successfully optimized our hardware selection—incorporating high-capacity options like the ARRIS SURFboard 33 modems and Netgear enterprise switches—keeping our final expenditures at RM 89,519.12 out of an available RM 2,000,000 allowance. It proved that choosing long-term component value over cheap alternatives prevents costly maintenance cycles down the road.

### 🔢 Task 5 & Task 6: VLSM Subnetting Architecture & Project Synthesis
* **Concepts Covered:** Enterprise VLSM allocation, large-scale bit-boundary calculation, subnet masking constraints, and collective team retrospectives.
* **Core Contribution:** Collaborated directly on computing the extensive Variable Length Subnet Masking schema for our base network block allocation (`10.64.0.0/12`). Managed strict host separations across multiple functional areas, mapping logical blocks (e.g., Embedded Labs, Cisco Networks, General Purpose spaces, and Staff Rooms) securely down to unique subnet addresses.
* **Reflection:** Task 5 was undoubtedly the most challenging mathematical milestone of the project. Breaking down massive address blocks without overlapping subnet boundaries or wasting thousands of potential host addresses showed me the ultimate value of precision engineering. Seeing our group’s diverse designs consolidate into a final, production-ready network portfolio was deeply satisfying and a true testament to our collective effort.
