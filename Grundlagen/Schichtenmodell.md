---
version: "0.3"
art: nachschlagewerk
herkunft: ki-material
stand: 2026-11-19
---

# Schichtenmodell

> **Entwurf.** Allgemeiner Teil des Schichtenmodells aus dem ersten Projekt, ohne dessen Werkzeug (Salt). In Klammern steht, was gesetzt ist; alles andere ist *(Vorschlag der KI)*. Produktnamen sind Beispiele.

Eine Landschaft wird auf zwei Arten gelesen:

- **technisch in Schichten:** Worauf läuft etwas?
- **fachlich in zwei Teilen:** Ein Dienst erbringt Nutzen; Infrastruktur ist Voraussetzung, dass er läuft. Probe: Läuft der Dienst ohne das nicht? *(gesetzt 2026-11-13)*

Anwendungen und Plattformen sind die Stellen, an denen Technik und Fachlichkeit sich treffen. *(gesetzt 2026-11-13)*

## Schichten

| # | Schicht | macht | Grenze | Probe | Beispiel |
| --- | --- | --- | --- | --- | --- |
| 1 | Netz | verbindet nach außen und zwischen Geräten | nur Physisches | | Anschluss, Kabel, Switch |
| 2 | Hardware | Rechner, auf denen alles läuft | Gerät mit Netzwerkkarte, Platten, Strom | | Server |
| 3 | Virtualisierung | macht aus Hardware austauschbare Maschinen | endet an der Hülle der VM | VM aus der Sicherung auf anderer Hardware starten | Proxmox |
| 4 | Betriebssystem | macht aus einer VM eine verwaltete Maschine | Systempakete ja, Anwendungsdaten nein | leere VM, ein Konfigurationslauf, Maschine erscheint in der Überwachung | Debian |
| 5 | Laufzeit | gibt Anwendungen eine austauschbare Hülle | Engine ja, Container nein | Testcontainer startet | Docker |
| 6 | Anwendung | Software, die Nutzen erbringt | mit Konfiguration und Daten | Probe aus dem Steckbrief | Frigate |

Offen *(gesetzt 2026-11-16)*: Steht eine Aufsicht, die andere Anwendungen steuert, als eigene Schicht 7 darüber, oder ist sie eine Anwendung?

## Regeln

1. Eine Schicht kennt nur die direkt darunter.
2. Schichten dürfen übersprungen werden, nie umgekehrt.
3. Daten gehören zur Anwendung. Danach richtet sich die Sicherung.
4. Container, die nur einer Anwendung dienen, sind Teil der Anwendung, keine Schicht. Prüffrage: Läuft A auf B?
5. Das Netz zieht sich durch jede Schicht: Kabel, Netzwerkkarte, virtueller Switch, Adresse, Container-Netz, Port.
6. Was Schaden anrichten kann, bekommt einen eigenen Baustein, statt einer Ausnahme im Allgemeinen.
7. Wiederherstellbar ohne sich selbst: Was die Landschaft verwaltet oder schützt und selbst in ihr läuft, braucht einen Weg zurück ohne sich.

## Beziehungen

| Beziehung | zwischen | Beispiel |
| --- | --- | --- |
| läuft auf | Schichten | Frigate läuft auf Docker |
| besteht aus | Anwendung und ihren Teilen | Paperless besteht aus Web, Redis, PostgreSQL |
| nutzt | Diensten und Plattformen | Frigate nutzt Home Assistant |

Geteilt wird erst, wenn ein Fall es verlangt. Nutzen mehrere Anwendungen denselben Baustein, wird er ausgebaut, bis er Plattform ist.

## Nutzensicherung in den Schichten

Jedes Werkzeug der Nutzensicherung (Verwaltung, Überwachung, Sicherung) hat zwei Teile:

| Teil | ist | Beispiel Überwachung |
| --- | --- | --- |
| zentraler Teil | ein eigener Dienst mit eigenem Nutzensatz für den Betreiber | Prometheus |
| Teil an jeder Maschine | bringt jeder Dienst mit; liegt in der Schicht Betriebssystem | node_exporter |

Die **Basis** einer Maschine ist die Summe dieser Teile.

## Offen

- Fehlen senkrechte Aufgaben wie Protokollierung und Wiederherstellung?
- Gehört die Übertragung auf ein Werkzeug (im ersten Projekt: Salt mit Rollen, Profilen, Pillar) als Beispiel in den Rahmen?

## Fassungen

| Version | Datum | Was sich ändert |
| --- | --- | --- |
| 0.1 | 2026-11-19 | Entwurf: allgemeiner Teil aus „Schichtenmodell und Salt-Struktur“ 0.3 und den Abweichungen |
| 0.2 | 2026-11-19 | Korrektur: ohne „Werkstück“ (gesetzt) |
| 0.3 | 2026-11-19 | Korrektur: Herkunft neutral „gesetzt“ statt „Meister“ |
