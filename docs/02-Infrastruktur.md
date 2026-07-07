# Infrastruktur

## Einleitung

Die Windows-Server-Infrastruktur wurde vollständig innerhalb einer Microsoft-Hyper-V-Umgebung aufgebaut.

Alle Server und Clients kommunizieren über ein gemeinsames internes Netzwerk und sind Mitglieder der Active-Directory-Domäne **firma.intern**.

Die Infrastruktur bildet die Grundlage für sämtliche in den folgenden Kapiteln beschriebenen Windows-Serverdienste.

---

## Virtuelle Maschinen

Für die Laborumgebung wurden folgende virtuelle Systeme eingerichtet:

- **DC** – Primärer Domänencontroller
- **DC1** – Zusätzlicher Domänencontroller
- **Router** – Standardgateway und DHCP-Server
- **FileServer** – Zentraler Dateiserver
- **WSUS** – Windows Server Update Services
- **WDS** – Windows Deployment Services
- **Windows 11** – Domänenclient
- **Windows 11 PXE** – Testclient für die Betriebssystembereitstellung

Jede virtuelle Maschine übernimmt innerhalb der Infrastruktur eine klar definierte Aufgabe.

---

## Netzwerk

Die gesamte Laborumgebung wurde im Netzwerk **192.168.10.0/24** aufgebaut.

Die automatische Vergabe der IP-Adressen erfolgt über den DHCP-Server. Die interne Namensauflösung wird durch den DNS-Dienst bereitgestellt.

Alle Systeme kommunizieren innerhalb derselben Domäne und greifen auf die zentral bereitgestellten Windows-Serverdienste zu.

---

## Domänenumgebung

Die Domäne **firma.intern** bildet die zentrale Verwaltungsinstanz der gesamten Infrastruktur.

Benutzer, Gruppen und Computer werden zentral über Active Directory verwaltet. Weitere Dienste wie DNS, DHCP, Dateiserver, Gruppenrichtlinien, WSUS und WDS sind in diese Domänenumgebung integriert.

---

## Zusammenfassung

Die eingerichtete Infrastruktur stellt die technische Grundlage für sämtliche in diesem Repository dokumentierten Windows-Serverrollen dar.

Die nachfolgenden Kapitel beschreiben die Konfiguration und Überprüfung der einzelnen Dienste im Detail.
