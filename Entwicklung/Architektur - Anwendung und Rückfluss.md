---
version: "0.3"
art: anleitung
herkunft: ki-material
stand: 2026-11-19
---

# Architektur - Anwendung und Rückfluss

> **Entwurf *(Vorschlag der KI)*.** Wie ein Projekt den [[Architekturrahmen]] für sich schärft und wie Lehren zurück in den Rahmen finden. Muss so konkret werden, dass jede KI weiß, was sie tun muss (gesetzt 2026-11-19). Ordnung dazu: [[Architektur - Entwicklungsordnung]].

Der Rahmen ist allgemein, jedes Projekt schärft ihn für sich. Was sich im Projekt bewährt, kann zurück in den Rahmen steigen. *(Mechanik: Vorschlag der KI; Anspruch gesetzt 2026-11-19)*

## Schärfen: vom Rahmen ins Projekt

1. **Übernehmen.** Jedes Projekt hat eine eigene Ordnung. Sie nennt, welche Fassung des Rahmens gilt, und übernimmt ihn, ohne ihn abzuschreiben.
2. **Schärfen.** Die Projektordnung ergänzt nur, was das Projekt braucht: eigene Begriffe, Orte, Werkzeuge, Dokumentarten.
3. **Begründet abweichen.** Allgemeines gilt, bis Spezifischeres widerspricht. Widerspricht die Projektordnung dem Rahmen, steht dort, warum.

## Zurückgeben: vom Projekt in den Rahmen

Lehren werden **an der Quelle getrennt**: Was das Projekt betrifft, bleibt im Projekt. Was den Rahmen betrifft, wird sofort im Rahmen festgehalten, sonst findet es den Weg nicht zurück (gesetzt 2026-11-19).

1. **Trennen.** Bei jeder Lehre und jeder bewährten Weise fragt die KI: Betrifft das nur dieses Projekt oder den Rahmen?
   - nur das Projekt → Abweichungsliste des Projekts
   - den Rahmen → Vorschlag im Eingang des Rahmens
2. **Vorschlagen.** Ein Vorschlag ist eine Datei in `_roh/Eingang/` des Rahmens: `<Datum> <Projekt> - <Thema>.md` mit Projekt, Anlass, was gelebt wird, welcher Teil des Rahmens berührt ist.
3. **Zusammenführen.** Im Rahmen werden die Vorschläge nach Thema gebündelt. Sagen zwei Projekte dasselbe, gilt es als bewährt.
4. **Setzen.** Der Verantwortliche des Rahmens setzt, was in den Rahmen steigt. Mit Git ist das der Merge nach `main`.

## Bezugswege

| Weg | Für wen | Schärfen | Zurückgeben |
| --- | --- | --- | --- |
| **Paket** | alle, ohne Git | Eine veröffentlichte Fassung (`X.0`) ins Projekt legen | Vorschlagsdateien an den Verantwortlichen des Rahmens geben; er legt sie in den Eingang |
| **Git** | Verantwortlicher des Rahmens | Rahmen-Repo ins Projekt ziehen | Vorschlagsdatei auf eigenem Ast `vorschlag/<projekt>-<thema>`, Merge-Request nach `main`; der Merge ist das Setzen |

## Offen

- Schritte so konkret fassen, dass eine KI sie ohne Rückfrage ausführt (Dateinamen, Vorlage der Abweichungsliste, wann fragen).
- Form des Pakets (eine Datei oder der Ordner als ZIP).
- Wie Git das Repo ins Projekt zieht (Submodul, Subtree oder Kopie).

## Fassungen

| Version | Datum | Was sich ändert |
| --- | --- | --- |
| 0.1 | 2026-11-19 | Entwurf: aus dem Kern übernommen, Bezugswege Paket und Git |
| 0.2 | 2026-11-19 | Ausarbeitung: Trennen an der Quelle, Eingang, Zusammenführen (gesetzt) |
| 0.3 | 2026-11-19 | Korrektur: Herkunft neutral „gesetzt“ statt „Meister“ |
