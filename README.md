<div align="center">

# 👋 Hey, I'm Craig aka **croogmandoo**

**Systems & Homelab Engineer · Automation Builder · Linux Tinkerer · Local AI Explorer**

Building resilient self-hosted infrastructure, automating workflows, and exploring local agentic systems.

[![Website](https://img.shields.io/badge/Website-croogmandoo.xyz-00E5FF?style=for-the-badge&logo=google-chrome&logoColor=black)](https://croogmandoo.xyz)
[![GitHub](https://img.shields.io/badge/GitHub-croogmandoo-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/croogmandoo)
[![Linux](https://img.shields.io/badge/Linux-CachyOS-1793D1?style=for-the-badge&logo=arch-linux&logoColor=white)](https://cachyos.org)
[![Proxmox](https://img.shields.io/badge/Hypervisor-Proxmox%20VE-E57000?style=for-the-badge&logo=proxmox&logoColor=white)](https://www.proxmox.com)
[![Docker](https://img.shields.io/badge/Containers-Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com)
[![Python](https://img.shields.io/badge/Automation-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org)

**Jump to:** [🧭 At a glance](#-at-a-glance) · [🧪 Homelab Stack](#-homelab-stack) · [🚀 Featured Projects](#-featured-projects) · [📊 GitHub Stats](#-github-stats) · [📫 Connect](#-connect)

</div>

---

## 🧭 At a glance

| | |
|---|---|
| 🛠️ **What I do** | Systems administration, homelab architecture, Docker containerization, workflow orchestration, and building practical automation tools. |
| 🐧 **Desktop & OS** | **CachyOS** (Arch Linux) as primary daily driver, leveraging performance-tuned kernels and bcachefs/ZFS for workstations. Ubuntu & Debian for production homelab servers. |
| 🏗️ **Homelab** | Multi-node virtualization under **Proxmox VE**, automated container deployments, GitOps configuration management, and continuous telemetry monitoring. [Detailed stack below.](#-homelab-stack) |
| 🤖 **AI & Automation** | Architecting local AI pipelines, Model Context Protocol (MCP) tooling, agentic orchestration, and Python-driven CLI engines. Pragmatic AI tooling paired with rigorous engineering. |
| ⚡ **Hardware & IoT** | Custom ESP32 display controllers, e-ink status dashboards, custom macropads, and home telemetry sensors. |
| 🧠 **Cares about** | Self-reliance & local compute, clean declarative infrastructure, telemetry & observability, reproducibility, privacy, and open tooling. |

> *"Own your compute, automate the repetitive toil, and keep the feedback loops short."*

---

## 🧪 Homelab Stack

A production-minded homelab designed for learning, testing, and hosting services with high availability, telemetry, and automated disaster recovery.

### 🖥️ Compute & Virtualization
- **Primary Hypervisor:** **Proxmox VE Cluster** hosting nested microservices, container runtimes, and isolated sandbox VMs.
- **Workstation:** AMD Ryzen 7 5800X (8C/16T), NVIDIA RTX 4070 (local inference & CUDA workloads), 32GB DDR4, high-speed NVMe storage.
- **Edge & SBCs:** Low-power embedded boards, ESP32 nodes, and dedicated low-draw compute instances for continuous services.

### 🌐 Networking & Security
- **Topology:** Segmented VLANs separating trusted LAN, IoT devices, guest network, and container overlays.
- **Zero-Trust & Remote Access:** Secure overlay networks with WireGuard and Cloudflare Tunnels (no open inbound management ports).
- **Internal DNS & Routing:** Dedicated split-horizon internal resolution under private domain zones (`.lanb4time.xyz`).
- **Secrets Management:** Encrypted secret storage via SOPS / Age keys, keeping sensitive credentials safely outside plain text repositories.

### 📊 Observability & Metrics
- **Metrics Collection:** **Prometheus** with **Node Exporter** and **Blackbox Exporter** probing service health and host vitals.
- **Log Aggregation:** **Grafana Loki** paired with **Promtail** streaming container and system logs.
- **Dashboards:** **Grafana** visualization for resource saturation, container uptime, and storage IOPS.
- **Alerting & Push Notifications:** **Alertmanager** coupled with self-hosted **Ntfy** for instant incident alerting on mobile and desktop.

### 💾 Storage & Data Persistence
- **Databases:** Production-configured **PostgreSQL** cluster with automated WAL (Write-Ahead Logging) archiving and base backups.
- **Storage Pools:** NVMe scratch spaces for heavy I/O, mirrored pools for container persistence, and SMB/NFS shares for distributed access.

---

## 🚀 Featured Projects

A curated selection of infrastructure stacks, automation tooling, and hardware builds.

### 🏗️ Homelab & Infrastructure

| Project | Description | Stack |
|---|---|---|
| **[croogmandoo.xyz](https://github.com/croogmandoo/croogmandoo.xyz)** | GitOps repository managing my homelab services, Ansible playbooks, Docker Compose stacks, and encrypted SOPS secrets. | `Ansible` `Docker` `Prometheus` `SOPS` |
| **[vmwarelab](https://github.com/croogmandoo/vmwarelab)** | Automated provisioning and lifecycle orchestration for nested virtualization environments (ESXi, vCenter, AD domain controllers) on Proxmox. | `Python` `Proxmox API` `Docker` `PowerCLI` |
| **[infrastructure-monorepo](https://github.com/croogmandoo/infrastructure-monorepo)** | Centralized configuration blueprints, container compose recipes, and reverse proxy definitions for private cloud hosting. | `Docker Compose` `Nginx` `WireGuard` |

### 🤖 Automation & Agentic Systems

| Project | Description | Stack |
|---|---|---|
| **[croogmindoo](https://github.com/croogmandoo/croogmindoo)** | Local assistant and workflow orchestrator integrating personal second-brain notes with homelab diagnostic APIs. | `Python` `MCP` `FastAPI` `Local LLM` |
| **[local-ai-tools](https://github.com/croogmandoo/local-ai-tools)** | Custom Model Context Protocol (MCP) server providing structured tools for Proxmox status, Docker management, DNS checks, and Obsidian vault ingest. | `Python` `MCP Protocol` `Proxmox API` |
| **[antigravity_phone_chat](https://github.com/croogmandoo/antigravity_phone_chat)** | Lightweight mobile-friendly interface for routing quick tasks and homelab notifications through local agent runners. | `Python` `WebSockets` `Tailscale` |

### ⚡ Embedded & Hardware

| Project | Description | Stack |
|---|---|---|
| **[esp32-ideasfor1.2tft](https://github.com/croogmandoo/esp32-ideasfor1.2tft)** | Microcontroller UI and telemetry firmware for miniature 1.2" round and square TFT displays showing real-time homelab stats. | `C++` `ESP-IDF` `PlatformIO` `LVGL` |
| **[custom-macropad](https://github.com/croogmandoo/custom-macropad)** | Custom mechanical macropad firmware and hardware layout optimized for developer workflows, window management, and terminal shortcuts. | `QMK` `Embedded C` `KiCad` |
| **[eink-esp32](https://github.com/croogmandoo/eink-esp32)** | Low-power E-Paper status board pulling daily agenda, server alerts, and environmental sensor readings over Wi-Fi. | `ESP32` `Arduino` `Deep Sleep` |

---

## 📊 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=croogmandoo&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="croogmandoo's GitHub Stats" />
<br />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=croogmandoo&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" />

</div>

---

## 🛠️ Tech Stack & Tooling

<div align="center">

| Area | Technologies |
|---|---|
| **Virtualization & OS** | Proxmox VE, Docker, Debian, Ubuntu Server, CachyOS, Linux Kernels |
| **Scripting & Languages** | Python, Bash, YAML, SQL, C++, Jinja2 |
| **Monitoring & Telemetry** | Prometheus, Grafana, Loki, Promtail, Alertmanager, Ntfy, Node Exporter |
| **Networking & Protocols** | VLANs, WireGuard, Cloudflare Tunnels, DNS, SMB, REST, WebSockets, MCP |
| **Tooling & Workflow** | Git, uv, Docker Compose, SOPS / Age, Obsidian, Make, VS Code / Antigravity |

</div>

---

## 📫 Connect

- 🌐 **Web:** [croogmandoo.xyz](https://croogmandoo.xyz)
- 🐙 **GitHub:** [@croogmandoo](https://github.com/croogmandoo)

---

<div align="center">
<sub>⚡ Built with curiosity · 🐧 Powered by Linux · 🛡️ Self-Hosted</sub>
</div>
