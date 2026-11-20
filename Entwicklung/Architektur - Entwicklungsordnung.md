---
version: "0.3"
art: ordnung
herkunft: ki-material
stand: 2026-11-19
---

# Architektur - Entwicklungsordnung

> **Entwurf *(Vorschlag der KI)*.** Regelt, wie der [[Architekturrahmen]] entsteht und gepflegt wird. Der Rahmen selbst sagt, wie ich Architekturarbeit mache; diese Ordnung sagt, wie der Rahmen wächst. Gegliedert nach Maxime (Richtung), Prinzip (Verbindung), Regel (Ordnung).

**Wesenskern.** Der Rahmen wächst aus bewährter Praxis und bleibt überall verständlich.

## Maximen

- **M1 Bewährt vor erdacht.** In den Rahmen kommt, was sich in einem Projekt bewährt hat.
- **M2 Eigenständig vor eingebunden.** Der Rahmen trägt sich selbst und gilt in jedem Projekt, ohne eines zu brauchen. *(Anspruch gesetzt 2026-11-19)*
- **M3 Verständlich vor vollständig.** Lieber wenige Sätze, die jeder versteht.

## Prinzipien

| Nr. | Prinzip | Maxime |
| --- | --- | --- |
| P1 | **Die Praxis führt.** Der Rahmen wächst aus dem, was Projekte festhalten. | M1 |
| P2 | **Was er braucht, steht in ihm.** Der Rahmen verweist nicht nach außen. | M2 |
| P3 | **Rahmen und Anwendung getrennt.** Der Rahmen sagt nur, was überall gilt; wie ein Projekt ihn anwendet, steht im Projekt. | M2 |
| P4 | **Jeder Satz besteht die Fragen** „Wem nützt es?“ und „Versteht man es?“ | M3 |

## Regeln

| Nr. | Regel | Prinzip |
| --- | --- | --- |
| R1 | **Samen.** `Architekturrahmen.md` ist der Kern; Rohes liegt in `_roh/`, die Entwicklung in `Entwicklung/`. | P2 |
| R2 | **Rückweg.** Eine neue Erkenntnis aus einem Projekt kommt zuerst nach `_roh/`; der Meister setzt, ob sie in den Rahmen steigt. | P1 |
| R3 | **Beispiele** sind als Beispiel gekennzeichnet. Ein Ordner `Beispiele/` entsteht erst mit dem zweiten Projekt. | P3 |
| R4 | **Kein Verweis nach außen** im Kern; `_roh/` darf auf Herkunft zeigen. | P2 |
| R5 | **Fassung.** Jede Änderung zählt `0.x` hoch und ergänzt die Fassungstabelle; `1.0` heißt: in einem zweiten Projekt bewährt. | P1 |
| R6 | **Eigenes Repo,** sobald ein zweites Projekt den Rahmen zieht. | P2 |

## Offen

- Maximen und Wesenskern setzt der Verantwortliche des Rahmens.
- Gelten die Maximen der Werkstattordnung (Wesen vor Prägung, Ermöglichen statt erzwingen, Integrität vor Wirkung) hier mit?

## Fassungen

| Version | Datum | Was sich ändert |
| --- | --- | --- |
| 0.1 | 2026-11-19 | Entwurf |
| 0.2 | 2026-11-19 | Ausarbeitung: Eigenständigkeit als Maxime M2 (gesetzt) |
| 0.3 | 2026-11-19 | Korrektur: Herkunft neutral „gesetzt“ statt „Meister“ |
