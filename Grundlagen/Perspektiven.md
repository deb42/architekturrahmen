---
version: "0.5"
art: nachschlagewerk
herkunft: ki-material
stand: 2026-11-19
---

# Perspektiven

> **Entwurf.** Drei Blicke auf denselben Dienst oder dieselbe Plattform, jeder für andere Leser. In Klammern steht, was gesetzt ist; alles andere ist *(Vorschlag der KI)*. Produktnamen sind Beispiele.

Jeder Dienst und jede Plattform lassen sich fachlich, konzeptionell und technisch beschreiben. Die drei Perspektiven sind sauber zu trennen. *(gesetzt 2026-11-17)*

## Die drei Perspektiven

| | **Fachlich** | **Konzeptionell** | **Technisch** |
| --- | --- | --- | --- |
| Frage | Was tut es, und für wen? | Aus welchen Arten von Bausteinen besteht es, und worauf läuft es? | Womit genau ist es gebaut? |
| Sprache | allgemein verständlich, ohne Technik; bildhafte Namen erlaubt | allgemeine Bausteinarten; Produkte nur als Beispiel | so nah wie möglich an den wirklichen Komponenten: echte Produktnamen |
| Leser | alle, zuerst der Nutzer | Architekt | Betreiber, Agent, der baut |
| Grundlage | Dienst und Infrastruktur, Teildienste, Fähigkeiten | Schichten, Bausteinarten, Beziehungen | Produkte, Maschinen, Code |
| Dokument (Beispiel) | Steckbrief | konzeptionelle Architektur, gegliedert nach Sichten | technische Architektur, Komponenten |

## Sichten der konzeptionellen Perspektive

Die konzeptionelle Perspektive wird in Sichten unterteilt. Jede Sicht beantwortet eine eigene Frage. *(gesetzt 2026-11-19)*

| Sicht | Frage | Begriffe | Beispiel |
| --- | --- | --- | --- |
| **Rollensicht** | Wer handelt, und wer darf was? | Rolle (Endnutzer, Betreiber, Agent), Freigabe, Aufsicht | Der Verantwortliche gibt frei, der Agent setzt um. |
| **Prozesssicht** | In welcher Folge geschieht was? | Aufgabe, Ablauf | Planungsdienst: erfassen, einordnen, abgleichen, erinnern |
| **Funktionssicht** | Was muss es können? | Fähigkeit, Teildienst | Agentenplattform: denken, beaufsichtigen, Notizbuch auslesen |
| **Datensicht** | Welche Information entsteht, wo liegt sie, wem gehört sie, wie fließt sie? | Information, Ablage, Fluss | Akte des Planungsdienstes, Aufnahmen der Kameras |
| **Anwendungssicht** | Welche Bausteine erbringen es, und worauf laufen sie? | Komponente, Schicht, Beziehung | Bausteine der Agentenplattform auf den Schichten |

Regeln:

1. **Die Sichten wählt der Fall.** Nicht jeder Fall braucht alle fünf. Gezeichnet wird, was eine Frage beantwortet.
2. **Eine Sicht, eine Frage.** Mischt ein Bild zwei Sichten, wird es geteilt.
3. **Die Datensicht folgt der Information, nicht der Technik.** Wo etwas technisch gespeichert ist, sagt die technische Perspektive.

## Regeln

1. **Von fachlich nach technisch.** Erst steht das fachliche Bild, dann folgen die Bausteine, dann die Technik. *(gesetzt 2026-11-16)*
2. **Jede Perspektive bleibt bei ihrer Sprache.** Fachlich keine Produktnamen, technisch keine Bilder. *(gesetzt 2026-11-17)*
3. **Die Zuordnung ist sichtbar.** Ein Architekturdokument zeigt in einer Spalte, welcher fachliche Name zu welchem technischen Baustein gehört. *(gesetzt 2026-11-17)*
4. **Im Code spricht nur die Technik.** Fachliche Namen stehen dort nur für Eigenkreationen, die es technisch sonst nicht gibt. *(gesetzt 2026-11-17)*
5. **Technische Architektur ohne Adressen.** Sie gilt für jede Instanz; Adressen und Zugriffswege stehen bei der einzelnen Komponente. *(gesetzt 2026-11-12)*

## Beispiel

Eine Plattform für KI-Agenten aus dem ersten Projekt:

| Fachlich | Konzeptionell | Technisch |
| --- | --- | --- |
| Aufsicht | Agentenaufsicht | Paperclip |
| Zelle | Agentenlaufzeit, eine je Agent | Hermes Agent in Docker |
| Denktor | LLM-Gateway | LiteLLM |
| Pforte | Reverse Proxy | Caddy |
| Außentor | Firewall | nftables |

## Zusammenhang

Die Perspektiven sind der Ort der **Verbindung** im Dreiklang: Die Sprache übersetzt zwischen ihnen, ohne dass sich die Richtung (der Nutzen) oder die Ordnung (das Gefüge) ändert.

## Offen

- Feste Regeln für Information stehen im [[Verwaltungsrahmen]] (Informationsordnung).

## Fassungen

| Version | Datum | Was sich ändert |
| --- | --- | --- |
| 0.1 | 2026-11-19 | Entwurf: aus den Abweichungen 12.11., 16.11., 17.11. und den Architekturdokumenten des ersten Projekts |
| 0.2 | 2026-11-19 | Ausarbeitung: fünf Sichten der konzeptionellen Perspektive (gesetzt); „funktional“ ist eine Sicht, „fachlich“ die Perspektive |
| 0.3 | 2026-11-19 | Korrektur: offene Frage zur Datensicht an den Verwaltungsrahmen verwiesen |
| 0.4 | 2026-11-19 | Korrektur: ohne „Werkstück“ (gesetzt) |
| 0.5 | 2026-11-19 | Korrektur: Herkunft neutral „gesetzt“ statt „Meister“ |
