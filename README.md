# Secure Local DNS Resolver & Traffic Analytics Engine

## 📌 Project Overview
An enterprise-grade network infrastructure deployment designed to optimize privacy, security, and real-time visibility across a local area network (LAN). Utilizing a headless Raspberry Pi architecture, this system acts as a secure local DNS resolver to block network-wide malicious domains while simultaneously sniffing local network interfaces for deep-packet traffic analytics.

---

## 🛠️ Architecture & Core Components
* **Hardware:** Headless Raspberry Pi (Debian Trixie 64-bit architecture)
* **DNS Sinkholing (Pi-hole):** Intercepts network-wide upstream DNS requests, mitigating ad-trackers, malware vectors, and telemetry scripts at the gateway level.
* **Traffic Inspection (ntopng):** Configured as a passive network probe executing deep packet inspection (DPI) to monitor throughput, identify anomalous behavioral spikes, and visualize active network protocol flows.

### Live Infrastructure Telemetry

<p align="center">
  <img src="images/pihole-dashboard.png" width="45%" alt="Pi-hole Secure DNS Analytics" />
  <img src="images/ntopng-dashboard.png" width="45%" alt="ntopng Deep Packet Inspection Flows" />
</p>
---

## ⚙️ Deployment & Configuration Highlights
* **Resource Optimization:** Adjusted kernel-level systemd journal constraints and storage allocation limits to protect internal SD card lifecycle states.
* **Service Isolation:** Managed web portal bindings to prevent interface conflicts across local network ports (`80` for admin routing, `3000` for deep packet analytics).
* **Traffic Baselining:** Implemented network interface listening criteria to isolate internal communication metrics from external WAN ingress traffic.

---

## 📈 System Observations & Insights
*(Once your 48-hour data collection finishes, you can type 2-3 sentences here about what kind of telemetry data your ntopng dashboard visualized, such as top protocols used or bandwidth distribution).*
