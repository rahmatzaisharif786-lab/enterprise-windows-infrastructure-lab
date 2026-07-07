# Projektbeschreibung

## Einleitung

Im Rahmen dieses Projekts wurde eine vollständige Windows-Server-Infrastruktur innerhalb einer Microsoft-Hyper-V-Umgebung aufgebaut und konfiguriert.

Ziel war die Bereitstellung einer zentral verwalteten Unternehmensumgebung, in der Benutzer, Computer, Netzwerkdienste und Dateifreigaben über Active Directory verwaltet werden.

Die gesamte Infrastruktur wurde in einer virtuellen Umgebung umgesetzt und besteht aus mehreren Windows-Servern sowie einem Windows-11-Client zur Funktionsprüfung.

---

## Projektziele

Während des Projekts wurden folgende Komponenten eingerichtet und konfiguriert:

- Hyper-V als Virtualisierungsplattform
- Active Directory Domain Services (AD DS)
- DNS
- DHCP
- Dateiserver mit Freigaben und NTFS-Berechtigungen
- Gruppenrichtlinien (GPO)
- Windows Server Update Services (WSUS)
- Windows Deployment Services (WDS)

---

## Verwendete Systeme

Für die Umsetzung des Projekts wurden folgende Systeme eingesetzt:

- **DC** – Primärer Domänencontroller
- **DC1** – Zusätzlicher Domänencontroller
- **Router** – DHCP-Server und Standardgateway
- **FileServer** – Bereitstellung von Dateifreigaben
- **WSUS** – Zentrale Verwaltung von Windows-Updates
- **WDS** – Netzwerkbasierte Windows-Bereitstellung
- **Windows 11** – Client zur Funktionsprüfung

---

## Projektumfang

Nach der Einrichtung der Serverrollen wurde die gesamte Infrastruktur getestet und auf ihre Funktionsfähigkeit überprüft.

Dabei wurden unter anderem folgende Bereiche validiert:

- Anmeldung eines Domänenbenutzers
- Automatische IP-Adressvergabe über DHCP
- Namensauflösung innerhalb der Domäne
- Anwendung von Gruppenrichtlinien
- Automatische Netzlaufwerkszuordnung
- Zugriff auf freigegebene Ordner entsprechend der vergebenen Berechtigungen
- Bereitstellung eines Windows-Clients über WDS
- Kommunikation mit dem WSUS-Server

Die einzelnen Komponenten sowie deren Konfiguration werden in den nachfolgenden Kapiteln ausführlich beschrieben.

---

## Virtuelle Laborumgebung

Die folgende Abbildung zeigt die in Microsoft Hyper-V eingerichtete Laborumgebung. Sämtliche virtuellen Maschinen wurden innerhalb dieser Umgebung erstellt und bilden gemeinsam die Grundlage der implementierten Windows-Server-Infrastruktur.

**Abbildung 1: Übersicht der virtuellen Maschinen in Hyper-V**

![Abbildung 1: Übersicht der virtuellen Maschinen in Hyper-V](../screenshots/01-HyperV.png)
