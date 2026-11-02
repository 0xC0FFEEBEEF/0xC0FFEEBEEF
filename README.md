## Hi, I'm Nathan

I build and document homelab infrastructure, self-hosted services and hands-on systems projects.
I work in IT, go to school alongside it, and learn best by building real things.
The full write-ups live on **[nbdevlab.com](https://www.nbdevlab.com)**.

### What I'm building

- **slerm**: a four-node Slurm cluster across two Proxmox hypervisors, built to learn Slurm end to end. Slurm
  compiled from source, a dedicated controller, shared NFS, MUNGE auth, cgroup-enforced scheduling, CPU and GPU
  partitions and job accounting. Its jobs process NOAA radar data, analyse Wazuh alerts, run software builds and
  serve local LLMs on two Tesla P100s.
- **Emergency power policy**: when the UPS loses mains, the main hypervisor sheds heavy VMs and containers, keeps
  DNS alive, powers down a second server through iDRAC, sets an iLO power cap, and restores everything when power
  returns. Core network services went from a few minutes of runtime to roughly 15–20.
- **Byteme R730**: a Dell PowerEdge R730 rebuilt as the lab's heavy compute and GPU node: HBA swap, Tesla P100s,
  CPU and RAM upgrade. Storage expansion is next.
- **AICMS**: scans my VMs, services and hypervisors, works out how they relate, and turns that into documentation
  an AI (and I) can use.
- **Security and monitoring**: Wazuh as the SIEM for every hypervisor, server and the VPS, with Zabbix and Grafana
  for health and trends.
- **nbdevlab.com**: React and TypeScript on Cloudflare Workers, D1 and R2, with a live status page fed by the lab
  and a public map of how it all fits together.

### The lab

Two Proxmox servers and a bare-metal node behind a WatchGuard Firebox, with a third Proxmox host parked:
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

- [hp-envy-fan](https://github.com/0xC0FFEEBEEF/hp-envy-fan): Linux fan-curve driver and KDE Plasma 6 widget for
  the HP ENVY x360 15 (board 876F)

Most of my lab code is private for now. When I'm not in the lab: gaming, D&D, and time with friends and family.

[nbdevlab.com](https://www.nbdevlab.com) · [Get in touch](https://www.nbdevlab.com/contact)
