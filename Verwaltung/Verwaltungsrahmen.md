---
version: "0.4"
art: rahmen
herkunft: ki-material
stand: 2026-11-19
---

# Verwaltungsrahmen

> **Entwurf.** Was die Architektur von der Verwaltung verlangt. Die Architektur gestaltet; sie verwaltet nicht selbst, stellt aber Anforderungen an die Verwaltung. *(gesetzt 2026-11-19)* Was nicht als gesetzt markiert ist, ist *(Vorschlag der KI)*.

**Wesenskern.** Verwaltung erhält, was gestaltet wurde.

Verwaltung ist ein Werkzeug der Nutzensicherung. Sie wird wie die Überwachung unterschieden in **Infrastrukturverwaltung** und **Dienstverwaltung**. *(gesetzt 2026-11-19)*

| | Infrastrukturverwaltung | Dienstverwaltung |
| --- | --- | --- |
| erhält | Komponenten: Geräte, Maschinen, Unterlagen, Plattformen | Dienste und ihre Information |
| für | den Betreiber | den Betreiber im Auftrag des Nutzers |
| Prüffrage | Läuft alles, worauf der Dienst angewiesen ist? | Nützt der Dienst noch, und ist seine Information in Ordnung? |
| Beispiel Werkzeug | Konfigurationsverwaltung (im ersten Projekt: Salt) | Steckbrief, Entwicklungsplan, Sicherung der Anwendungsdaten |

Jedes Werkzeug der Verwaltung hat einen zentralen Teil, der selbst ein Dienst für den Betreiber ist, und einen Teil an jeder Maschine, den jeder Dienst mitbringt (siehe [[Schichtenmodell]]).

## Infrastrukturverwaltung

### Übergabe

Jede Komponente wird **an die Infrastrukturverwaltung übergeben**. *(gesetzt 2026-11-19; im ersten Projekt gelebt als „Maschine an Salt übergeben“)* Eine Komponente ist übergeben, wenn:

| Nr. | Bedingung | Prüffrage |
| --- | --- | --- |
| U1 | sie **eingetragen** ist: Name, Bauart, Standort, verwaltet ja oder nein | Steht sie im Verzeichnis? |
| U2 | ihr **Verantwortlicher** feststeht: der Dienst, dem sie dient, oder die Plattform selbst | Wer ist zuständig? |
| U3 | die **Werkzeuge der Verwaltung** ihren Teil an ihr tragen, soweit ihre Art es zulässt | Wird sie überwacht, gesichert, aktuell gehalten? |

Was eine Komponente nicht leisten kann (etwa ein Gerät ohne eigenen Verwaltungsteil), steht bei ihr als bewusste Lücke.

### Anforderungen

| Nr. | Anforderung | Prüffrage |
| --- | --- | --- |
| K1 | **Nachvollziehbar eingerichtet.** Jede Einrichtung ist beschrieben und wiederholbar, nicht von Hand. | Ließe sie sich gleich noch einmal bauen? |
| K2 | **Aktuell.** Komponenten werden auf Stand gehalten, ohne dass etwas bricht. | Wer hält sie aktuell? |
| K3 | **Wiederherstellbar ohne sich selbst.** Was die Landschaft verwaltet, braucht einen Weg zurück ohne sich. | Wie komme ich hinein, wenn es selbst ausfällt? |

## Dienstverwaltung

### Dienste

Ein Dienst ist **voll ausgebaut**, wenn er funktioniert und dafür gesorgt ist, dass er weiter funktioniert. Wie weit man ausbaut, richtet sich nach dem Aufwand. *(gesetzt 2026-11-19)* Dazu gehört, dass alle seine Komponenten übergeben sind.

| Nr. | Anforderung | Prüffrage |
| --- | --- | --- |
| D1 | **Bemerkt.** Fällt ein Dienst aus, merkt es jemand, bevor der Nutzer es sagt. | Wer merkt den Ausfall? |
| D2 | **Wiederherstellbar.** Ein Dienst lässt sich aus Beschreibung und Sicherung neu aufbauen. | Bekomme ich ihn zurück? |
| D3 | **Beschrieben.** Was der Dienst kann und wohin er wächst, steht an einem Ort. | Wo steht, was er kann und was noch kommt? |

### Information

Die **Informationsordnung** sagt, was mit Information geschieht, unabhängig davon, wo sie technisch liegt.

| Nr. | Anforderung | Prüffrage |
| --- | --- | --- |
| I1 | **Eigentum.** Jede Information hat einen Eigentümer, der über sie entscheidet. | Wem gehört sie? |
| I2 | **Ort.** Jede Information hat genau einen führenden Ort; Kopien sind als Kopien erkennbar. | Wo ist das Original? |
| I3 | **Aufbewahrung.** Jede Information hat eine Frist, wie lange sie bleibt. | Wann darf sie weg? |
| I4 | **Weitergabe.** Information verlässt die eigene Landschaft nur über einen benannten Weg. | Wohin darf sie, und auf welchem Weg? |
| I5 | **Daten gehören zur Anwendung.** Danach richtet sich die Sicherung. | Mit welcher Anwendung wird sie zurückgespielt? |

## Offen

- Ab wann braucht ein Projekt die Informationsordnung vollständig, und was reicht für den Anfang?
- Gehören Rückbau und das geordnete Ende eines Dienstes hierher?
- Wird die Information später eine eigene, dritte Verwaltung?

## Fassungen

| Version | Datum | Was sich ändert |
| --- | --- | --- |
| 0.1 | 2026-11-19 | Entwurf: Informationsordnung und Anforderungen an Dienste |
| 0.2 | 2026-11-19 | Ausarbeitung: Übergabe von Komponenten (gesetzt) |
| 0.3 | 2026-11-19 | Strukturierung: Infrastrukturverwaltung und Dienstverwaltung (gesetzt) |
| 0.4 | 2026-11-19 | Korrektur: Herkunft neutral „gesetzt“ statt „Meister“ |
