# Cybersecurity Home Lab for Ethical Hacking & Network Security

I built a cybersecurity home lab to practice both attacking and defending systems.  
The lab uses Kali Linux as the attacker and Ubuntu as the target. Both machines run in VirtualBox on a NAT network so everything is safe and isolated from my main computer.

---

## 🖥 Setting Up the Environment
On Ubuntu, I updated the system and installed essential tools like build-essential, git, curl, and wget. I also checked its IP address using ip a so Kali could reach it.

On Kali Linux, I updated the OS and installed key security tools such as nmap, Wireshark, and metasploit-framework. This setup gave me a realistic environment for testing both attacks and defenses.

---

## 🔍 Performing Network Scans
From Kali, I ran nmap -A with Ubuntu's IP to see which ports were open and what services were running. For example, FTP was open on port 20.

This step simulates reconnaissance, which is the phase attackers use to gather information before attempting a breach. It helped me understand how attackers think and plan.

---

## 🛡 Defending Ubuntu with UFW Firewall
To protect Ubuntu, I installed the UFW firewall. I allowed SSH connections so I could manage the system remotely and only allowed traffic from Kali's IP. All other connections were blocked.

This setup lets me safely test attacks while keeping the target secure from unwanted traffic.

---

## 📊 Analyzing Traffic with Wireshark
On Ubuntu, I used Wireshark to capture and analyze network traffic while Kali performed attacks. I watched the TCP handshake packets like SYN, SYN-ACK, and RST, which helped me understand how connections work and how attacks progress on the network.

---

## 🎯 Skills Developed
- Understanding attacks and defenses from both red team and blue team perspectives  
- Linux system administration and command-line usage  
- Firewall setup and network protection  
- Network traffic monitoring and packet analysis  
- Using virtualization to create safe test environments  

---

This project gave me hands-on experience with both attacking and defending systems. It helped me improve my understanding of how attackers operate and how defenders can respond, while building practical skills in Linux, networking, and cybersecurity tools.
