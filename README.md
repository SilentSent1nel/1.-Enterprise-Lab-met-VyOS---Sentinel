# 1. Enterprise Lab met-VyOS

Dit project is een zelfstandig aangemaakt en opgebouwd netwerk en serverlab in VMware Workstation Pro.
Het doel van het project is het ontwerpen, configureren en testen van een gescheiden netwerk infrastructuur 
met meerdere servers en netwerk zones.

## Infrastructuur

Het netwerk bestaat uit de volgende componenten:

- DH-EDGE-01: VyOS router en firewall
- DH-WEB-01: Nginx webserver
- DH-APP-01: Samba fileserver
- DH-MGMT-01: Beheerserver
- DH-CLIENT-1 / DH-CLIENT-2: Client systemen

## Netwerksegmenten

| Zone |     Subnet     |     Functie    |
| ---- | -------------- | -------------- |
| LAN  | 172.16.20.0/24 | Client netwerk |
| DMZ  | 172.16.25.0/24 |     Servers    |
| MGMT | 172.16.30.0/24 |     Beheer     |

## Services

### Nginx

DH-WEB-01 draait als webserver met Nginx. De webserver is vanuit de clientomgeving getest.

### Samba

DH-APP-01 biedt een SMB fileshare aan via Samba. De share is vanaf een Windows-client getest met authenticatie.

## Netwerkbeveiliging

DH-EDGE-01 gebruikt zone-based firewall met policies tussen LAN, DMZ, MGMT en WAN.
De firewall policy gebruikt standaard een deny/drop principe waarbij alleen specifieke verkeer wordt toegelaten.

## Configuratiebeheer

De configuraties en documentatie van het project worden bijgehouden in deze repository.

## Doel van het project

Middels deze project oefen ik praktische vaardigheden op het gebied van:

- VMware
- Linux serverbeheer
- Netwerkconfiguratie
- Routing
- Firewalling
- Nginx
- Samba/SMB
- Netwerksegmentatie
- Configuratiebeheer en Git

Het project wordt telkens uitgebreid en gedocumenteerd, ook te zien aan de Git commit geschiedenis binnen deze repository.


## Eindbewijs

Het volledige eindbewijs van dit project is beschikbaar via:
1. Voorpagina van dit repository onder de naam: "Enterprise Lab met VyOS - Eindbewijs", het is een .pdf bestand.
2. Via: [Documentatie](https://github.com/SilentSent1nel/1.-Enterprise-Lab-met-VyOS---Sentinel/blob/main/Enterprise%20Lab%20met%20VyOS%20-%20Eindbewijs.pdf)
