# 3. Traffic-Analyse mit Wireshark

**Datum:** XX.06.2026  
**Ziel:** Den Netzwerkverkehr während des vsftpd-Exploits untersuchen und die Indikatoren für einen Angriff (IOCs) identifizieren.

## Vorgehen
- Wireshark auf `eth0` (Host-only) gestartet, Filter später auf `ftp` gesetzt.
- Exploit aus Übung 2 ausgeführt.

## Beobachtungen
- Im FTP-Stream sieht man die Sequenz:
  USER u:) (Benutzername mit Smiley) und PASS XjL
- Direkt danach wird ein neuer TCP-Port geöffnet, über den die Shell läuft.
- Ein IDS/IPS hätte diese ungewöhnliche Zeichenkombination im FTP-Traffic erkennen und blockieren können.

## Verteidigungsansatz
- Suricata/Snort-Regeln könnten auf den String `USER.*:\)` im FTP-Traffic prüfen.
- Netzwerksegmentierung: FTP-Verkehr gehört nicht in ein unsicheres Subnetz.

## Screenshot
https://github.com/ds20cs/cybersec-lab/blob/main/assets/screenshots/wireshark_ftp_exploit.png
