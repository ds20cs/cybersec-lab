# 1. Nmap-Scan gegen Metasploitable

**Datum:** 15.06.2026  
**Ziel:** Offene Ports, laufende Dienste und Betriebssystem des Opfers erkennen.

## Ausgeführte Befehle
```bash
ping 192.168.70.129                          # Erreichbarkeitstest
sudo nmap -sS -p- 192.168.70.129             # Schneller Scan aller Ports
sudo nmap -sV -O 192.168.70.129              # Service- und OS-Erkennung

Screenshot: https://github.com/ds20cs/cybersec-lab/blob/main/assets/screenshots/nmap_scan.png?raw=true
