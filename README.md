## Hi, I'm Nathan

I build and document homelab infrastructure, self-hosted services and hands-on systems projects.
I work in IT, go to school alongside it, and learn best by building real things.
The full write-ups live on **[nbdevlab.com](https://www.nbdevlab.com)**.

### What I'm building

- **[slerm](https://github.com/0xC0FFEEBEEF/slerm-cluster)**: a four-node Slurm cluster across two Proxmox hypervisors, built to learn Slurm end to end. Slurm
  compiled from source, a dedicated controller, shared NFS, MUNGE auth, cgroup-enforced scheduling, CPU and GPU
  partitions and job accounting. Its jobs process NOAA radar data, analyse Wazuh alerts, run software builds and
  serve local LLMs on two Tesla P100s.
- **[Emergency power policy](https://github.com/0xC0FFEEBEEF/homelab-power-plan)**: when the UPS loses mains, the main hypervisor sheds heavy VMs and containers, keeps
  DNS alive, powers down a second server through iDRAC, sets an iLO power cap, and restores everything when power
  returns. Core network services went from a few minutes of runtime to roughly 15–20.
- **byteme2, HP ProLiant DL360 Gen9**: the main Proxmox hypervisor (2× Xeon E5-2683 v4, 32 cores / 64 threads, 64 GB, ZFS).
  It runs the house services and DNS, and decides what happens when the power goes out.
- **byteme, Dell PowerEdge R730**: rebuilt as the lab's heavy compute and GPU node, now 2× Xeon E5-2695 v4
  (36 cores / 72 threads) and 64 GB: HBA swap, two Tesla P100s, CPU and RAM upgrade. Storage expansion is next.
- **byteme3, HP ProLiant DL380 Gen9**: 2× Xeon E5-2690 v3 (24 cores / 48 threads) with 10 TB of storage installed, waiting on RAM before
  it comes back online.
- **deadlock**: a bare-metal Intel server that runs as a slerm node. It stays off when idle and wakes when jobs
  need it.
- **[AICMS](https://github.com/0xC0FFEEBEEF/aicms-homelab)**: scans my VMs, services and hypervisors, works out how they relate, and turns that into documentation
  an AI (and I) can use.
- **Security and monitoring**: Wazuh as the SIEM for every hypervisor, server and the VPS, with Zabbix and Grafana
  for health and trends.
- **[nbdevlab.com](https://github.com/0xC0FFEEBEEF/nbdevlab-site)**: React and TypeScript on Cloudflare Workers, D1 and R2, with a live status page fed by the lab
  and a public map of how it all fits together.

### The lab

Two Proxmox servers and a bare-metal node behind a WatchGuard Firebox, with the DL380 waiting on RAM:
144 CPU threads, 160 GB of RAM, 12 TiB of ZFS and two Tesla P100s. There are no inbound ports at home;
everything comes in over Cloudflare Tunnel, WireGuard or Tailscale. It also runs Nextcloud, Home Assistant,
Gitea, Pi-hole, Jellyfin, Proxmox Backup Server and Proxmox Mail Gateway.

[Homelab map](https://www.nbdevlab.com/homelab) · [Live status](https://www.nbdevlab.com/status) · [All projects](https://www.nbdevlab.com/projects)

### Toolbox

- **Systems**: Windows Server, Active Directory, Group Policy, DNS, DHCP, WSUS, DFS, IIS, Microsoft 365
- **Virtualization**: Proxmox, Hyper-V, Ubuntu Server, Debian, Arch Linux, backups, UPS automation
- **Monitoring and security**: Wazuh, Zabbix, Grafana, log review, alerting, hardening, active response
- **Networking and access**: TCP/IP, VLANs, firewall rules, SSH, Cloudflare Zero Trust, remote administration
- **Automation**: Bash, scripting, GAM, CLI tools, backup automation, dashboards
- **Hardware**: helpdesk, endpoint repair, PC builds, screen and keyboard replacement, basic solder rework

### Public code

**The lab**
- [slerm-cluster](https://github.com/0xC0FFEEBEEF/slerm-cluster): the Slurm cluster's control panel, job pipelines, gateway and P100 work
- [homelab-power-plan](https://github.com/0xC0FFEEBEEF/homelab-power-plan): the UPS guardian, guest restore and outage dashboard
- [homelab-topology-map](https://github.com/0xC0FFEEBEEF/homelab-topology-map): the generator behind the [homelab map](https://www.nbdevlab.com/homelab)
- [homelab-status-fob](https://github.com/0xC0FFEEBEEF/homelab-status-fob): an ESP8266 OLED key fob showing live lab status
- [aicms-homelab](https://github.com/0xC0FFEEBEEF/aicms-homelab): inventories hosts over SSH and turns scans into documentation

**AI tooling on local models**
- [open-webui-code-mode](https://github.com/0xC0FFEEBEEF/open-webui-code-mode): a Chat | Code switch for Open WebUI, one coding agent per chat
- [openwebui-computer-agent](https://github.com/0xC0FFEEBEEF/openwebui-computer-agent): a model drives a real desktop from a chat
- [owl-openwebui-cli](https://github.com/0xC0FFEEBEEF/owl-openwebui-cli): a terminal coding agent for Open WebUI, forked from Codex CLI
- [llm-shared-memory](https://github.com/0xC0FFEEBEEF/llm-shared-memory): one conversation memory shared by Claude Code, Codex and local models
- [zsh-ai-companion](https://github.com/0xC0FFEEBEEF/zsh-ai-companion): an AI assistant that lives in the zsh prompt

**Web, hardware and fun**
- [nbdevlab-site](https://github.com/0xC0FFEEBEEF/nbdevlab-site): the source of nbdevlab.com
- [hp-envy-fan](https://github.com/0xC0FFEEBEEF/hp-envy-fan): Linux fan-curve driver and KDE Plasma 6 widget for the HP ENVY x360 15
- [cubepro-klipper-cura](https://github.com/0xC0FFEEBEEF/cubepro-klipper-cura): Cura profile for a Cube Pro running Klipper
- [cyclops-voice-fx](https://github.com/0xC0FFEEBEEF/cyclops-voice-fx): makes any TTS voice sound like the Subnautica Cyclops
- [dice-king-leaderboard](https://github.com/0xC0FFEEBEEF/dice-king-leaderboard): a D&D dice-collection leaderboard on Cloudflare Workers

When I'm not in the lab: gaming, D&D, and time with friends and family.

[nbdevlab.com](https://www.nbdevlab.com) · [Get in touch](https://www.nbdevlab.com/contact)
