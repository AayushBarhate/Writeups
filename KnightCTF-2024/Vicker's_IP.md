# Vicker's IP CTF Writeup

## Analyzing the Packets

Utilizing Wireshark to open the provided `packets-file.pcapng`, I meticulously searched through the packets. Within the HTTP objects, I stumbled upon "nikto," a web server scanner used by attackers to gather information about their targets.

## Unveiling the Attacker and Victim IPs

Further investigation led me to a packet where "nikto" was mentioned, indicating a transfer from IP address `192.168.1.7` (attacker) to `192.168.1.8` (victim). Armed with this information, I successfully identified the attacker and victim IPs.

![packets](<images/Vickers.png>)

## Obtaining the Flag

With the attacker and victim IPs in hand, I extracted the flag: `KCTF{192.168.1.8_192.168.1.7}`.
