# Snort IDS Detection Lab

Basic IDS detection and attack mitigation lab using Snort, Nmap, Kali Linux, and iptables.

This project demonstrates beginner-level SOC analyst skills by simulating suspicious network activity, detecting scans using the Snort Intrusion Detection System (IDS), and applying firewall rules to mitigate potentially malicious traffic.

The lab was performed inside a Kali Linux virtual machine using local traffic simulation and basic defensive security techniques.

---

# Skills Demonstrated

- Linux terminal usage
- IDS monitoring
- Network traffic analysis
- Attack simulation
- Snort configuration
- Nmap reconnaissance scanning
- Firewall mitigation with iptables
- Security event investigation
- Basic incident response

---

# Environment

- Kali Linux
- VirtualBox
- Snort IDS
- Nmap
- iptables
# Snort Installation Verification

```bash
snort -V
```

![Snort Version](snort_version.jpg)

This output confirms that Snort 3 was successfully installed on Kali Linux and that the IDS engine is available for network traffic monitoring and analysis.

---

# Snort Configuration Validation

![Snort Validation]<img width="1527" height="807" alt="Snort successfully validated the configuration" src="https://github.com/user-attachments/assets/0ee60d0e-53ba-418b-8b00-d63226e9eb3e" />
)

The Snort configuration was successfully validated, confirming that the IDS modules, rule sets, and packet inspection engine were correctly initialized before starting traffic analysis.

---

# Initial Nmap Reconnaissance Scan

```bash
nmap localhost
```

![Nmap Local Scan](!<img width="1020" height="641" alt="nmap localhost" src="https://github.com/user-attachments/assets/bdb3484d-0efb-42c2-ab8b-d090d25892b1" />
]()
 )

This scan simulates basic reconnaissance activity against the localhost system before defensive firewall rules were applied.

---

# Snort Detection and Traffic Monitoring

![Snort Detection](snort_detection_alert.png.jpg)

Snort monitored local network traffic and detected suspicious scanning activity generated during the Nmap reconnaissance simulation.

---

# Firewall Mitigation Rules

```bash
sudo iptables -L
```

![Firewall Rules](firewall_rule_added.jpg)

Firewall rules were added using iptables to block suspicious localhost scanning activity and restrict potentially malicious TCP SYN traffic.

---

# Blocked Nmap Scan After Mitigation

```bash
nmap localhost
```

![Blocked Nmap Scan](nmap_scan_blocked.jpg)

After applying the firewall mitigation rules, the Nmap scan became significantly slower and less effective, demonstrating successful traffic restriction and defensive filtering.
