# Vicker's PCAP Analysis CTF Writeup

## Analyzing the PCAP File

Utilizing NetworkMiner, a software that lists probable services and their versions based on network packets, I examined the provided pcap file. Focusing on the victim's IP address `192.168.1.8`, I sought to identify vulnerable services.

## Identifying the Vulnerable Service

NetworkMiner revealed that the victim was running vsftpd version 2.3.4, which I recognized as a known vulnerable service. To confirm its vulnerability, I cross-referenced the service and version on Google, validating its susceptibility to exploitation.

## Obtaining the Flag

With vsftpd 2.3.4 identified as the vulnerable service, I extracted the flag: `KCTF{vsftpd_2.3.4}`.

