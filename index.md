---
layout: home
title: Home
---

## About me

I am Inaam Verteneuille, a cybersecurity student currently on an exchange semester at Universiti Malaya in Malaysia. I am in the final year of a work-study Master's programme at ESIEE-IT in France, and I work for an insurance company as a Cybersecurity Reporting Analyst (*Chargé de pilotage Cyber Sécurité*). In this role, I collect cybersecurity KPIs, turn them into clear dashboards, and improve the way this data is gathered.

## Technical skills

### Development

| Skill | Level | Demonstrated in |
|-------|-------|-----------------|
| SQL | Working knowledge | BTS SIO SLAM, work-study |
| Python | Confident | Bachelor's projects, work-study |
| JavaScript | Beginner | BTS SIO SLAM |
| Java | Beginner | BTS SIO SLAM |
| C# | Beginner | BTS SIO SLAM |
| Web development (HTML, CSS) | Working knowledge | BTS SIO SLAM |
| Secure development (OWASP Top 10) | Working knowledge | Bachelor's degree (Secure Digital Solutions Developer) |

### Networking

| Skill | Level | Demonstrated in |
|-------|-------|-----------------|
| TCP/IP fundamentals | Working knowledge | Cisco ITN |
| VLANs and routing | Beginner | Cisco SRWE |
| Cisco Packet Tracer | Working knowledge | Cisco ITN, WQE7007 labs |
| Wireshark | Working knowledge | Cisco CyberOps labs, Bachelor's projects |

### Systems

| Skill | Level | Demonstrated in |
|-------|-------|-----------------|
| Linux (command line, administration) | Working knowledge | [Virtual lab setup](projects/virtual-lab-setup/) |
| Windows | Working knowledge | Work-study |
| Virtualisation (VirtualBox, UTM) | Working knowledge | [Virtual lab setup](projects/virtual-lab-setup/) |

### Offensive security

| Skill | Level | Demonstrated in |
|-------|-------|-----------------|
| Nmap | Working knowledge | [Nmap service scan](projects/nmap-service-scan/) |
| Penetration testing methodology | Beginner | [Nmap service scan](projects/nmap-service-scan/), WQE7011 |
| Metasploit | Beginner | WQE7011 labs |
| Burp Suite | Working knowledge | Bachelor's projects, Work-Study |

### Defensive security

| Skill | Level | Demonstrated in |
|-------|-------|-----------------|
| Log analysis | Beginner | Cisco CyberOps labs |
| SIEM | Beginner | Cisco CyberOps labs |
| Incident response | Beginner | Cisco CyberOps |
| Malware analysis | Beginner | Cisco CyberOps |

### Governance and compliance

| Skill | Level | Demonstrated in |
|-------|-------|-----------------|
| GDPR | Working knowledge | CNIL training |
| Protection of classified information | Working knowledge | DRSD training |
| Risk management | Beginner | WIX3003 |

### Tools

| Skill | Level | Demonstrated in |
|-------|-------|-----------------|
| Git and GitHub | Working knowledge | [This repository](https://github.com/InaamV/cybersecurity-portfolio) |
| Docker | Beginner | Bachelor's projects |
| Bash scripting | Beginner | Work-study |

### Business applications

| Skill | Level | Demonstrated in |
|-------|-------|-----------------|
| Microsoft Power Apps | Working knowledge | Work-study |
| Microsoft Power Automate | Working knowledge | Work-study |
| Microsoft Power BI | Beginner | Work-study |
| Microsoft Excel | Beginner | Work-study |

## Education

- **Master's degree in Cybersecurity - E3IN** (work-study) - ESIEE-IT, France - 2025-2027 (in progress)
  - Exchange semester at Universiti Malaya, Malaysia - Sept. 2026-Feb. 2027
- **Bachelor's degree: Secure Digital Solutions Developer** (*Développeur de solutions numériques sécurisées*) - ESIEE-IT, France - 2025
- **Bachelor's degree (Licence) in Cybersecurity** - CNAM, France - 2025
- **Higher National Diploma (BTS) in IT Services for Organisations, Software Solutions and Business Applications option (SIO SLAM)** - ESIEE-IT, France - 2024

## Certifications and training

**Completed**
- **Protection of Classified Information** (*La protection des secrets*) - Direction du Renseignement et de la Sécurité de la Défense (DRSD), 2023
- **GDPR and its key concepts - Module 1** (*Le RGPD et ses notions clés*) - CNIL, 2023
- **Cisco Introduction to Networks (ITN)** - Cisco Networking Academy, 2026

**In progress**
- **Cisco Switching, Routing and Wireless Essentials (SRWE)** - Cisco Networking Academy - target: December 2026
- **Cisco CyberOps Associate** (WQE7001 Cyber Security, Universiti Malaya) - Cisco Networking Academy - target: December 2026

**Planned**
- **Cisco Enterprise Networking, Security and Automation (ENSA)**

## Projects

- [Virtual lab setup](projects/virtual-lab-setup/)
- [Nmap service scan](projects/nmap-service-scan/)

## Learning journey

### Building a safe lab

The first lab I worked on was building an isolated virtual lab. On my Mac M1, I could not use VirtualBox to run x86 machines, so I learned to use UTM and to combine a virtualised Kali Linux (ARM) with an emulated Metasploitable 2. The most important lesson was isolation: I connected both machines on a host-only network and tested it myself, by checking that Kali could reach Metasploitable but not the Internet. I learned that a lab is only safe if you verify it, not just configure it.

### Scanning with Nmap

The second lab was a service scan of Metasploitable 2 with Nmap. It is closely linked to the first one: a scan must only target systems you control or are authorised to test, and my isolated lab gave me exactly that. With a single `nmap -sV` command, I found 23 open ports and their versions. What surprised me most was how much this information reveals: by researching the versions, I found a root shell on port 1524 and a known backdoor in vsftpd 2.3.4. This showed me why every unnecessary open port increases the attack surface.

### Something that went wrong

When I first started Metasploitable 2, it did not boot: instead of the login screen, I landed on a UEFI Interactive Shell. I did not know what this shell was, so I searched for the error online and found that other people had faced the same problem with UTM. Their explanations helped me diagnose it: UTM enables UEFI boot by default for new virtual machines, but Metasploitable 2 is an old system that only supports legacy BIOS boot. I disabled UEFI boot in the virtual machine's settings, and the machine started normally. This taught me that when I am stuck, documentation and other people's experience are often the fastest way to understand a problem, and that older systems need to be checked for compatibility before the first start.

### What I still find challenging

VLANs and routing are still difficult for me. My background is mostly in development and cybersecurity rather than networking, so the configuration labs in WQE7007 took me more time than other topics. I understand the concepts, but configuring and troubleshooting them on my own is not yet natural.

### My improvement goal

My goal is to build the first version of my SOC training application by the beginning of 2027. It will let users analyse realistic logs from my own lab and get an explanation at the end. I will measure my progress with a simple criterion: the first version must contain three complete scenarios, each with logs, questions and an explanation, that I can solve from start to finish myself. Building it will force me to understand log analysis in depth, which is the skill I need most for a SOC analyst role.

## Career objective

My target role is **SOC Analyst (Level 1)**. Working in a Security Operations Centre would give me hands-on experience in detecting and responding to real threats, and it opens many paths in cybersecurity.

After completing my Master's in 2027, I would like to build on my current role as a Cybersecurity Reporting Analyst, which gives me a broad view of my company's security through its KPIs. Alongside it, I will prepare for a SOC position through three concrete steps:

1. Complete the Cisco CyberOps Associate course by December 2026, then pass the Cisco CyberOps Associate (CBROPS) certification by June 2027.
2. Build my own SOC training application, in which users analyse realistic logs and get an explanation at the end. A first version with three scenarios is planned for the beginning of 2027.
3. Practise with SIEM tools through the TryHackMe SOC Level 1 path.

In the longer term, I would also like to explore penetration testing, the goal I described in my earlier learning plan. Understanding attacks from the defensive side will give me a solid foundation for it.

## Contact

- Email: verteneuilleinaam@gmail.com
- GitHub: [InaamV](https://github.com/InaamV)
- LinkedIn: [Inaam Verteneuille](https://www.linkedin.com/in/inaam-verteneuille/)