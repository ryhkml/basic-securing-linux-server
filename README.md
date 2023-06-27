## Installation packages

This is the basic step i always do when securing Linux server

```bash
curl -s https://raw.githubusercontent.com/ryhkml/basic-securing-linux-server/main/init-deb | sudo bash
```

## Packages

1. <b>Unattended-upgrades</b>, is a feature in Debian and Ubuntu-based Linux distributions that allows you to automatically install security and other updates without any user intervention. This can be useful for servers or other systems that are not regularly monitored or used by humans

2. <b>Uncomplicated Firewall</b>, is a command-line firewall application for Linux distributions that aims to be easy to use for beginners while still providing a powerful firewall. It is a front-end for iptables, the standard Linux firewall, and uses a simple set of commands to manage firewall rules

3. <b>CrowdSec</b>, is an open-source, collaborative security suite that uses a crowdsourced approach to detect and block malicious traffic. It is designed to be easy to use and deploy, and can be used to protect any Linux server or device. CrowdSec works by monitoring your server for signs of malicious activity. If it detects an attack, it will block the offending IP address and report it to the CrowdSec community. The community will then analyze the attack and add it to the CrowdSec database, so that other users can be protected from it in the future

4. <b>NTP-Client</b>, in Linux is a software that synchronizes the system clock of a Linux computer with an NTP server. NTP stands for Network Time Protocol, and it is a protocol that allows computers to synchronize their clocks over the network

5. <b>Rkhunter</b>, is a security tool for Linux systems that scans for rootkits, backdoors, and other potential security vulnerabilities. It does this by checking for a variety of signs of compromise. Rkhunter is a valuable tool for any Linux system administrator who wants to protect their system from security threats. It is easy to use, and it can be very effective at detecting rootkits and other malicious software.

## Next steps

For more advanced, you can visit: https://github.com/imthenachoman/How-To-Secure-A-Linux-Server