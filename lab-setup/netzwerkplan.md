# Netzwerkplan

| Maschine        | Rolle                | OS                  | IP-Adresse         | RAM   | vCPU |
|-----------------|----------------------|---------------------|--------------------|-------|------|
| Kali            | Angreifer            | Kali Linux 2024.x   | **192.168.70.128**  | 2 GB  | 4    |
| Metasploitable2 | Opfer                | Ubuntu 8.04         | **192.168.70.129**  | 512 MB| 2    |
| Wireshark       | Verteidiger/Analyse  | (auf Kali)          | wie Kali           | -     | -    |

**Netzwerk:** Alle Maschinen hängen an einem VMware Host-only Adapter (`VMnet1`).  
Subnetz: `192.168.70.0/24`. Keine externe Erreichbarkeit.

**Monitoring:** Wireshark läuft direkt auf Kali und zeichnet sämtlichen Traffic auf dem Host-only-Interface auf. Damit können Angriffe aus Sicht des Netzwerks analysiert werden (z.B. Protokollanomalien, Exploit-Patterns).

**Screenshots:**  
https://github.com/ds20cs/cybersec-lab/blob/main/assets/screenshots/netzwerkplan_beweis_kali.png?raw=true

https://github.com/ds20cs/cybersec-lab/blob/main/assets/screenshots/netzwerkplan_beweis_metasploitable2.png?raw=true
