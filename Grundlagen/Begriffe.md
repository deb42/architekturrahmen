---
version: "0.3"
art: nachschlagewerk
herkunft: ki-material
stand: 2026-11-19
---

# Begriffe

> **Entwurf.** Die Kernbegriffe des [[Architekturrahmen|Architekturrahmens]], übernommen aus dem ersten Projekt und von dessen Werkzeugen gelöst. In Klammern steht, was gesetzt ist; alles andere ist *(Vorschlag der KI)*. Produktnamen sind Beispiele.

## Nutzen

| Begriff | Bedeutung | Prüffrage |
| --- | --- | --- |
| **Dienst** | erbringt einem Menschen Nutzen und hat dafür einen eigenen Nutzensatz in Ich-Form. Er trägt die Rolle, für die er Nutzen erbringt: Endnutzer oder Betreiber. *(gesetzt 2026-11-13, 2026-11-18)* | Wer hat den Nutzen, und nützt es allein? |
| **Rolle** | in welcher Eigenschaft jemand handelt oder Nutzen hat: Endnutzer, Betreiber, Agent | Wer handelt hier, und wer darf was? |
| **Teildienst** | eine Grundfunktion eines Dienstes, beschrieben mit „Ich kann …“ *(gesetzt 2026-11-12)* | Kann man es schon nutzen? |
| **Aufgabe** | was ein Dienst tut; sie nutzt Fähigkeiten *(gesetzt 2026-11-18)* | |
| **Fähigkeit** | besitzt eine Plattform; nützt allein niemandem und kann von mehreren Diensten genutzt werden. Ein Dienst **bestellt** Fähigkeiten bei einer Plattform. *(gesetzt 2026-11-18)* | Nützt es allein? Nein: Fähigkeit. |
| **Infrastruktur** | Voraussetzung, dass ein Dienst läuft *(gesetzt 2026-11-13)* | Läuft der Dienst ohne das nicht? |
| **Nutzensicherung** | sorgt dafür, dass ein Dienst weiter funktioniert. Werkzeuge sind Verwaltung, Überwachung und Sicherung. *(gesetzt 2026-11-19)* | Merke ich, wenn es ausfällt, und bekomme ich es zurück? |

**Voll ausgebaut** ist ein Dienst, wenn er funktioniert und dafür gesorgt ist, dass er weiter funktioniert. Wie weit man ausbaut, richtet sich nach dem Aufwand. *(gesetzt 2026-11-19)*

## Bau

| Begriff | Bedeutung | Beispiel |
| --- | --- | --- |
| **Komponente** | ein Teil, das man einzeln benennen, einrichten und ersetzen kann *(gesetzt 2026-11-12)* | Kamera, Frigate, Proxmox-Host |
| **Anwendung** | eine Einheit, die selbst Nutzen erbringt und als Ganzes betrieben wird *(gesetzt 2026-11-12)*. Probe: Wird es gemeinsam aktualisiert und zurückgespielt? | Frigate mit go2rtc |
| **Plattform** | bündelt Nutzen und ist dafür ausgebaut, dass mehreres dauerhaft darauf aufbaut *(gesetzt 2026-11-12)*. Sie ist keine Schicht und kann auf jeder entstehen. | Proxmox, Home Assistant |
| **Unterlage** | etwas läuft darauf, ohne dass sie dafür ausgebaut ist *(gesetzt 2026-11-12)* | Docker auf einer einzelnen VM |
| **Rückgrat** | trägt genau einen Dienst | Frigate für die Videoüberwachung |
| **Aufbau** | was ein Dienst auf einer Plattform baut | eine Automation in Home Assistant |

Zwei Arten von Plattform *(gesetzt 2026-11-13)*: Eine **Infrastrukturplattform** ermöglicht Dienste und ist für den Nutzer unsichtbar (Proxmox). Eine **Dienstplattform** ermöglicht Endnutzen; der Nutzer arbeitet mit ihr (Home Assistant).

**Verantwortung:** Ein Dienst verantwortet alle Komponenten, die nur ihm dienen, bis zu einer Plattform. Plattformen verantworten sich selbst. *(gesetzt 2026-11-12)*

## Ort

| Begriff | Bedeutung |
| --- | --- |
| **Landschaft** | alles zusammen, was jemand betreibt |
| **Standort** | der Ort, an dem Komponenten stehen; man kann ihn benennen, aber nicht ersetzen. Ordnungsbegriff, keine Komponente. *(gesetzt 2026-11-13)* |
| **Maschine** | alles, was im Netz eines Standorts eine Adresse hat. Container zählen nicht; sie sind Teil ihrer Maschine. Eigenschaft: verwaltet oder nicht. *(gesetzt 2026-11-13)* |
| **Bauart** | welche Art Maschine oder Komponente es ist; verfeinerbar, nur so tief, wie ein Fall es verlangt (Router → Fritzbox). *(gesetzt 2026-11-13)* |
| **Typ und Instanz** | Der Typ sagt, was für jede Ausprägung gilt, und heißt nach dem Produkt. Die Instanz ist die einzelne Ausprägung und heißt nach der Maschine oder einem Eigennamen. *(gesetzt 2026-11-12)* |

**Allgemeines gilt, bis Spezifischeres widerspricht.** Reihenfolge, das Spätere gewinnt: Standort, Bauart, Maschine. *(gesetzt 2026-11-13)*

## Arbeit

| Begriff | Bedeutung |
| --- | --- |
| **Vorhaben** | das große Ganze an einem Gegenstand *(gesetzt 2026-11-18)* |
| **Inkrement** | ein Schritt mit sichtbarem Nutzen; löst einen oder mehrere Aufträge aus *(gesetzt 2026-11-18)* |
| **Auftrag** | eine abgegrenzte Arbeit mit Gegenstand und Art (Aufbau, Ausbau, Pflege, Rückbau) und genau einem Protokoll *(gesetzt 2026-11-10, 2026-11-18)* |
| **Zielbild** | wohin ein Dienst wachsen soll; Inkremente führen schrittweise dorthin |

## Offen

- Im ersten Projekt heißen die Werkzeuge der Nutzensicherung noch „Plattformdienste“. Der Begriff entfällt hier, weil „Plattform“ einen eigenen Wesenskern hat.
- Wie heißt die Fähigkeit eines einzelnen Agenten im Rahmen („Agentenfähigkeit“) – gehört das in den Rahmen oder nur in Projekte mit Agenten?

## Fassungen

| Version | Datum | Was sich ändert |
| --- | --- | --- |
| 0.1 | 2026-11-19 | Entwurf: aus Dienst, Plattform, Komponente, Anwendung, Standort und den Abweichungen des ersten Projekts |
| 0.2 | 2026-11-19 | Ausarbeitung: Rolle |
| 0.3 | 2026-11-19 | Korrektur: Herkunft neutral „gesetzt“ statt „Meister“ |
