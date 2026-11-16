# Kleines Netzwerk - Simulation / Lernprojekt

## Ziel
Ein simuliertes kleines Firmen-Netzwerk aufbauen, IP-Adressen vergeben und die Verbindung testen.

Wichtig: Dies ist ein Lernprojekt / Simulation, kein echtes Heimnetzwerk.

## Aufbau
Router -> Switch -> PC1, PC2, Server, Drucker, Handy

## IP-Plan
Netz: 192.168.10.0 / 24
Subnet: 255.255.255.0
Gateway: 192.168.10.1
DNS: 8.8.8.8

| Gerät | IP-Adresse | Gateway |
| --- | --- | --- |
| Router | 192.168.10.1 | - |
| PC1 - Buchhaltung | 192.168.10.10 | 192.168.10.1 |
| PC2 - Lager | 192.168.10.11 | 192.168.10.1 |
| Server - Dateien | 192.168.10.20 | 192.168.10.1 |
| Drucker | 192.168.10.30 | 192.168.10.1 |
| Handy | 192.168.10.50 | 192.168.10.1 |

DHCP: 192.168.10.100 bis 192.168.10.150 für Gäste

## Ping-Test
PC1 -> PC2: Reply, erfolgreich
PC1 -> Server: Reply, erfolgreich
PC1 -> 8.8.8.8: Reply, erfolgreich, Internet ok

## Testfall / Problem und Lösung
Testfall: PC2 bekommt keine Verbindung.
Ursache: Gateway war falsch eingetragen: 192.168.10.2 statt 192.168.10.1.
Lösung: Gateway auf 192.168.10.1 korrigiert, danach Ping wieder erfolgreich.

## Was ich gelernt habe
IP-Adressen, Subnetmaske, Gateway, DNS, DHCP, Ping-Test, Dokumentation, Fehlersuche
