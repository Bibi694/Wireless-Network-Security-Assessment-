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
