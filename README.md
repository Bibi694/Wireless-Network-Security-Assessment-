# Wireless-Network-Security-Assessment-
🛡 Wireless Network Security Assessment

🎯 Overview

This project focuses on evaluating Wi-Fi network security, understanding how common wireless attacks work, and recommending strong protection strategies.
It was carried out in a controlled Kali Linux lab environment using virtual radios (mac80211_hwsim) to simulate Wi-Fi interfaces, since no physical USB adapter was available.

⸻

🧩 Objective

To demonstrate key wireless security concepts including:
	•	Capturing WPA2/WPA3 handshakes
	•	Cracking weak Wi-Fi passwords using dictionary attacks
	•	Exploring Rogue Access Point (Evil Twin) attack scenarios
	•	Recommending secure configurations and preventive policies

⸻

⚙ Lab Setup

Environment: Kali Linux (Virtual Machine)
Interfaces Simulated:
	•	wlan0 → Access Point (AP)
	•	wlan1 → Client/Victim
	•	wlan2 → Monitor Interface
	
Tools Used:
	•	Aircrack-ng – for capture and cracking
	•	Wireshark – for packet analysis
	•	Hostapd – to simulate a wireless access point
	•	wpa_supplicant – to simulate a wireless client
	•	Python – for basic captive portal scripting
	•	mac80211_hwsim – to create virtual radio

⸻

🧠 Tasks Performed

🧩 Task 1 — WPA2 Handshake Capture
	•	Created three virtual radios using mac80211_hwsim.
	•	Configured wlan0 as AP, wlan1 as client, and wlan2 as monitor.
	•	Captured the 4-way WPA handshake using airodump-ng.
	•	Verified handshake in the .cap file.
	
🔐 Task 2 — Weak Password Cracking
	•	Used rockyou.txt wordlist for a dictionary attack.
	•	Decompressed the wordlist and ran aircrack-ng against the captured handshake.
	•	Successfully recovered weak passwords, proving the risk of simple passphrases.
	
	⚠ Task 3 — Rogue AP / Evil Twin Simulation
	•	Outlined the process of simulating a fake AP to trick users.
	•	Unable to perform live demo due to missing USB Wi-Fi adapter.
	•	Documented reproducible steps for physical testing.

	🧾 Task 4 — Security Recommendations

Recommendations based on identified vulnerabilities:
	1.	Upgrade all APs to WPA3-Enterprise for stronger encryption.
	2.	Segment networks by department (Admin, Staff, Guest).
	3.	Implement RADIUS Authentication (802.1X) for individual access control.
	4.	Use strong passwords and rotate them periodically.
	5.	Conduct routine wireless penetration tests.
	6.	Train users to avoid fake Wi-Fi networks.

	🧠 Findings Summary
	#
Observation
Risk
1
Weak Wi-Fi password (password123)
Easy to crack
2
Automatic reconnection after deauth
Handshake captured easily
3
No network segmentation
Increases lateral attack surface
4
Shared Wi-Fi credentials
Poor user accountability
5
WPA2 instead of WPA3
Vulnerable to offline attacks
