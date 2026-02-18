# Kickoff Workshop Slide-Set
## Ergosoft x Asuno -- AI-gestuetzte Knowledge Base

---

## Folie 1 -- Titelfolie

# Ergosoft x Asuno
## AI-gestuetzte Knowledge Base
### Kickoff Workshop

Februar 2026

---

## Folie 2 -- Zielbild: Warum wird die Knowledge Base gebaut?

**Eine zentrale, AI-gestuetzte Wissensplattform fuer Ergosoft -- kein Wiki, kein Chatbot, sondern ein Hybrid-Ansatz.**

- Ergosoft verfuegt ueber umfangreiches Fachwissen, das aktuell verstreut und schwer auffindbar ist
- Mitarbeitende verbringen uebermässig viel Zeit mit der Suche nach Informationen ueber Loop, Z:-Laufwerk und direkte Rueckfragen bei Kollegen
- Vertrauen in bestehende Dokumentation ist gering -- veraltete Inhalte auf dem Z:-Laufwerk untergraben die Zuverlaessigkeit
- Wissensabhaengigkeit von Einzelpersonen (z.B. Eric, Alex) erzeugt Engpaesse bei der Eskalation
- Fabian hat eine klare Vision formuliert: "Klare Struktur, intelligente Suche" -- die Knowledge Base soll als strategische Infrastruktur das Fundament fuer effizienteren Support, besseres Onboarding und langfristig auch eine kundenorientierte Wissensplattform bilden

---

## Folie 3 -- Status Quo und Pain Points

**Die heutigen Probleme wurden direkt aus Stakeholder-Interviews abgeleitet.**

- **Verstreute Informationen:** Wissen ist ueber Loop, Z:-Laufwerk und muendliche Weitergabe fragmentiert -- es gibt keinen zentralen Anlaufpunkt
- **Vertrauensprobleme:** Das Z:-Laufwerk ist "voll mit veralteten Informationen" -- Mitarbeitende wissen nicht, ob Inhalte noch aktuell und korrekt sind
- **Wissens-Silos:** Kritisches Fachwissen liegt bei einzelnen Personen (z.B. TI-Wissen bei Eric, Support-Expertise bei Alexandra) -- hoher Bus-Faktor
- **Eskalationsengpaesse:** Support-Mitarbeitende muessen bei komplexen Fragen Kolleginnen und Kollegen direkt fragen, statt selbststaendig Antworten zu finden -- das blockiert beide Seiten
- **Fehlende Transparenz:** Fuehrungskraefte wissen nicht, ob ihre Dokumentation gefunden und genutzt wird (Albert: "Ich weiss nicht, ob meine Dokumente gefunden und genutzt werden")
- **Kein strukturierter Onboarding-Pfad:** Neue Mitarbeitende muessen sich Wissen selbst zusammensuchen -- Fabian-Prioritaet

---

## Folie 4 -- Loesungsansatz: AI-gestuetzte interne Knowledge Base

**Kombination aus strukturierten Artikeln und semantischer Suche -- kein reines Wiki, kein reiner Chatbot.**

- **Hybrid-Ansatz:** Strukturierte Wissensartikel mit Kategorien, Tags und Versionierung werden mit einer AI-gestuetzten semantischen Suche (RAG-Pipeline) kombiniert
- **AI-Suche (Retrieval-Augmented Generation):** Nutzeranfragen werden in Vektordarstellungen umgewandelt, gegen eine Vektor-Datenbank abgeglichen und mit traditioneller Volltextsuche kombiniert -- die AI generiert praezise Antworten mit Quellenangaben
- **Kein reines Wiki:** Das Problem ist nicht das Fehlen von Dokumenten -- Mitarbeitende haben bereits Dokumente, sie finden und vertrauen ihnen nur nicht. Die AI-Schicht ist der Differenzierungsfaktor
- **Kein reiner Chatbot:** Die Plattform basiert auf kuratierten, strukturierten Artikeln als Grundlage -- die AI durchsucht und synthetisiert diese, statt frei zu generieren
- **Einfacher Tech-Stack:** Next.js, Supabase (Postgres + pgvector), Vercel -- ein kompakter, wartungsarmer Stack, der Kosten niedrig und Komplexitaet gering haelt

---

## Folie 5 -- User Stories MVP (US-1 bis US-5)

**Die MVP-User-Stories adressieren die kritischsten Pain Points aus den Stakeholder-Interviews.**

| # | User Story | Begruendung | Prioritaet |
|---|-----------|-------------|------------|
| US-1 | Als Support-Mitarbeitender moechte ich an einem zentralen Ort mit Stichworten oder natuerlicher Sprache suchen, damit ich aufhoere, in Loop, Z:-Laufwerk und bei Kollegen zu suchen | Pain Point Nr. 1 -- verstreute Informationen | MVP |
| US-2 | Als Support-Mitarbeitender im Kundengespraech moechte ich sofortige, praezise Antworten auf Fehlermeldungen und haeufige Probleme, damit ich ohne Eskalation loesen kann | Reduziert den "Frag Eric oder Alex"-Engpass | MVP |
| US-3 | Als Wissenstraeger moechte ich schnell Artikel erstellen und aktualisieren (mit Markdown, Tags, Kategorien), damit Dokumentation keine Last ist | Dokumentationshuerden bemerkt von Albert, Eric, Alexandra | MVP |
| US-4 | Als Mitarbeitender moechte ich Artikel als veraltet oder fehlerhaft markieren koennen, damit die Wissensqualitaet hoch bleibt | Z:-Laufwerk "voll mit veralteten Infos" -- Vertrauen ist entscheidend | MVP |
| US-5 | Als Mitarbeitender moechte ich sehen, wann ein Artikel zuletzt aktualisiert wurde und von wem, damit ich die Zuverlaessigkeit einschaetzen kann | Vertrauensprobleme mit bestehender Dokumentation | MVP |

---

## Folie 6 -- User Stories MVP (US-6 bis US-9)

**Ergaenzende MVP-Stories decken FAQ, Struktur, Benachrichtigungen und Analytik ab.**

| # | User Story | Begruendung | Prioritaet |
|---|-----------|-------------|------------|
| US-6 | Als HR/Management moechte ich einen FAQ-Bereich fuer wiederkehrende unternehmensweite Fragen (Urlaub, Arbeitszeiten, Kuendigungsbedingungen) | Ann-Sophies Pain Point Nr. 1 -- der Wegweiser braucht ein besseres Zuhause | MVP |
| US-7 | Als Administrator moechte ich Inhalte nach Abteilung, Kategorie und Tags organisieren, damit die Knowledge Base von Tag eins eine klare Struktur hat | Fabian: "Klare Struktur, intelligente Suche" | MVP |
| US-8 | Als Mitarbeitender moechte ich benachrichtigt werden, wenn Artikel, die fuer meine Rolle relevant sind, erstellt oder aktualisiert werden | Eric: "Ich erfahre es erst, wenn Dinge nicht mehr funktionieren" | MVP |
| US-9 | Als Fuehrungskraft moechte ich grundlegende Analysen sehen (Suchen ohne Ergebnis, meistgesehene Artikel, veraltete Inhalte) | Albert: "Ich weiss nicht, ob meine Dokumente gefunden und genutzt werden" | MVP |

---

## Folie 7 -- User Stories nach Modulen: Uebersicht

**Die User Stories sind nach funktionalen Modulen gruppiert, um die Entwicklungssequenz abzubilden.**

| Modul | Beschreibung | User Stories | Phase |
|-------|-------------|-------------|-------|
| Modul 1: Wissensartikel (Kern-Inhalte) | Das Fundament -- alles andere baut darauf auf | US-3, US-5, US-7, US-4, US-17 | MVP (US-17: V2) |
| Modul 2: AI-Suche und Antworten | Der Differenzierungsfaktor -- darum ist das kein normales Wiki | US-1, US-2 | MVP |
| Modul 3: FAQ und wiederkehrendes Wissen | Schnelle Erfolge fuer hochfrequente, einfache Fragen | US-6, US-10, US-13 | MVP (US-10, US-13: V2) |
| Modul 4: Benachrichtigungen und Aenderungsmanagement | Loest das Problem "Ich erfahre es erst, wenn etwas kaputtgeht" | US-8 | MVP |
| Modul 5: Analytik und Wissensgesundheit | Sichtbarkeit ueber Luecken und Nutzung -- treibt kontinuierliche Verbesserung | US-9, US-12 | MVP (US-12: V2) |
| Modul 6: Onboarding-Pfade | Strukturiertes Lernen fuer neue Mitarbeitende -- Fabian-Prioritaet | US-11 | V2 |
| Modul 7: Externe Kunden-Knowledge-Base | Der strategische Langzeit-Plan -- kundenorientiert | US-14, US-15, US-16 | V3 |

---

## Folie 8 -- Roadmap V2: Geplante Erweiterungen

**V2-Stories stellen geplante Erweiterungen nach dem initialen MVP-Release dar, priorisiert nach Stakeholder-Input und strategischem Wert.**

| # | User Story | Modul |
|---|-----------|-------|
| US-10 | Als Support-Mitarbeitender moechte ich gefuehrte Fehlerbehebungsablaeufe fuer TI-Probleme (Firewall, Konnektor, Routing) | FAQ und wiederkehrendes Wissen |
| US-11 | Als neuer Mitarbeitender moechte ich einen strukturierten Onboarding-Pfad fuer meine Rolle mit aufeinander aufbauenden Lernmodulen | Onboarding-Pfade (Fabian-Prioritaet) |
| US-12 | Als Fuehrungskraft moechte ich ein "Bus-Faktor"-Dashboard, das zeigt, welche Wissensbereiche von einzelnen Personen abhaengen | Analytik und Wissensgesundheit |
| US-13 | Als Prozessverantwortlicher moechte ich interaktive Checklisten fuer komplexe wiederkehrende Prozesse (Rechnungslauf, SEPA, Onboarding) | FAQ und wiederkehrendes Wissen |
| US-17 | Als Management moechte ich, dass das System automatisch Artikel aus aufgenommenen Quellen vorschlaegt (Loop-Seiten, Server-Dokumente) | Wissensartikel |

---

## Folie 9 -- Roadmap V3: Strategischer Langzeit-Plan

**V3 ist der strategische, kundenorientierte Ausbau -- Fabians langfristige Vision.**

| # | User Story | Beschreibung |
|---|-----------|-------------|
| US-14 | Als Kunde moechte ich eine externe Wissensplattform / ein digitales Handbuch, um selbststaendig Fragen zur psychodat-Nutzung zu klaeren | Strategische Vision von Fabian -- kundenorientierte Knowledge Base |
| US-15 | Als Kunde moechte ich kontextsensitive Hilfe direkt innerhalb der psychodat-Module | In-App-Hilfe fuer psychodat |
| US-16 | Als Kunde moechte ich visuelle Schritt-fuer-Schritt-Anleitungen und kurze Videos fuer komplexe Arbeitsablaeufe | Visuelle Guides und Video-Inhalte |

**Strategische Einordnung:**
- V3 erweitert die interne Knowledge Base zu einer externen, kundenorientierten Plattform
- Kunden koennen psychodat-Fragen selbststaendig loesen, ohne den Support zu kontaktieren
- Kontextsensitive Hilfe direkt in der Anwendung reduziert Support-Anfragen an der Quelle
- Visuelle Anleitungen und Videos adressieren komplexe Workflows, die textbasiert schwer vermittelbar sind

---

## Folie 10 -- Architektur: Design-Philosophie

**Wir bauen eine AI-gestuetzte interne Knowledge Base -- kein Wiki, kein Chatbot, sondern einen Hybrid, der strukturierte Artikel mit semantischer Suche und AI-gestuetzten Antworten kombiniert.**

- **Frontend:** Next.js + Tailwind -- schnelle, moderne Oberflaeche; Fabian: "modern, klar, professionell"; Server-Side Rendering (SSR) fuer Geschwindigkeit
- **Backend/API:** Next.js API-Routes + Supabase -- Postgres, Authentifizierung, Echtzeit und Speicher in einem Paket; minimaler Infrastruktur-Overhead
- **Datenbank:** Supabase Postgres + pgvector -- relationale Daten fuer Artikel/Nutzer/Tags + Vektor-Embeddings fuer semantische Suche in einer Datenbank
- **AI/Suche:** Modell-agnostisch + Embeddings -- GPT, Claude, Gemini fuer Antwortgenerierung (RAG); Embeddings ueber Voyage oder OpenAI fuer Vektorsuche
- **Deployment:** Vercel + Supabase -- Standard-Stack mit schnellen Deployments und Preview-Umgebungen; Supabase auf Frankfurter Servern
- **Benachrichtigungen:** E-Mail (Resend) + In-App -- Artikel-Update-Benachrichtigungen gemaess US-8

---

## Folie 11 -- Architektur: So funktioniert die AI-Suche (RAG-Pipeline)

**Die Retrieval-Augmented Generation Pipeline kombiniert Vektor-Aehnlichkeitssuche mit traditioneller Stichwortsuche fuer maximale Abdeckung und Praezision.**

| Schritt | Aktion | Beschreibung |
|---------|--------|-------------|
| 1 | Anfrage einbetten (Embed Query) | Nutzeranfrage in eine Vektordarstellung umwandeln |
| 2 | Vektorsuche (Vector Search) | pgvector nach den Top-K aehnlichsten Artikelabschnitten durchsuchen |
| 3 | Stichwortsuche (Keyword Search) | Volltextsuche ueber Postgres tsvector ausfuehren |
| 4 | Hybride Zusammenfuehrung (Hybrid Merge) | Vektor- und Stichwortergebnisse fuer beste Abdeckung kombinieren |
| 5 | Kontextaufbereitung (Context Assembly) | Gefundene Abschnitte zusammen mit der Anfrage an die Claude API uebergeben |
| 6 | Antwortgenerierung (Answer Generation) | Claude generiert eine praezise Antwort mit Quellenverweisen |
| 7 | Anzeige (Display) | Antwort anzeigen mit Links zu den vollstaendigen Quellartikeln |

---

## Folie 12 -- Architektur-Entscheidungen: Warum dieser Stack?

**Jede Technologieentscheidung wurde bewusst getroffen, um Komplexitaet und Kosten niedrig zu halten.**

- **Warum Supabase + pgvector statt Pinecone/Weaviate?**
  - Ein Service weniger zu verwalten
  - pgvector ist ausreichend leistungsfaehig fuer die Ergosoft-Skalierung (Hunderte bis niedrige Tausende Artikel, nicht Millionen)
  - Haelt Kosten niedrig und den Stack einfach

- **Warum RAG statt Fine-Tuning?**
  - Inhalte aendern sich haeufig (quartalsweise Releases, TI-Updates, Prozessaenderungen)
  - RAG ermoeglicht die Aktualisierung der Knowledge Base ohne erneutes Training
  - Artikel werden beim Speichern neu eingebettet (re-embedded)

- **Warum kein reines Wiki (Notion/Confluence)?**
  - Fabian moechte explizit AI-gestuetzte Suche und kontextuelle Antworten, nicht nur Dokumentenablage
  - Die Interview-Daten zeigen: Mitarbeitende haben bereits Dokumente -- sie finden und vertrauen ihnen nur nicht
  - Die AI-Schicht ist der Differenzierungsfaktor

---

## Folie 13 -- Content-Strategie: Wie gelangen Inhalte ins System? (MVP)

**Fuer das MVP gelangt Content auf vier Wegen in das System.**

- **Manuelle Erstellung:** Mitarbeitende schreiben Artikel in einem Rich-Text-Editor
- **Massenimport (Bulk Import):** Einmaliges Migrationsskript, um bestehende Dokumente aus Loop und dem Z:-Laufwerk zu uebernehmen (docx/pdf werden geparst und in Artikel umgewandelt)
- **AI-gestuetztes Drafting:** Rohe Notizen oder einen Support-Fall einfuegen, die AI erstellt einen strukturierten Artikelentwurf, der Autor prueft und veroeffentlicht
- **Sprache zu Text (Voice to Text):** Einsatz von Whisper ermoeglicht nahtloseren Wissens-Upload und Dokumentationserstellung

---

## Folie 14 -- Vorgeschlagene Kategoriestruktur

**Basierend auf den Stakeholder-Interviews wurden folgende natuerliche Wissensdomaenen identifiziert.**

- **Kundenservice / Support**
  - TI-Troubleshooting (ePA, eRezept, eAU, Konnektor, Gateway)
  - psychodat Fehlerbehebung
  - Hardware und Netzwerk
  - Haeufige Kundenfragen
- **Vertrieb**
  - Produkte und Preise
  - Abos und Kuendigungen
  - Sondervereinbarungen
- **Buchhaltung und Finanzen**
  - Rechnungslauf
  - SEPA
  - embloom Abrechnung
- **Ambulanzen (AMBO)**
- **Personal / HR**
  - Wegweiser (Arbeitszeiten, Urlaub, etc.)
  - Onboarding
- **IT / Infrastruktur**
- **Prozesse und Ablaeufe**
- **Changelog / Neuigkeiten**

---

## Folie 15 -- Build Order: Entwicklungsreihenfolge

**Die Entwicklung ist so sequenziert, dass jedes Modul auf dem vorherigen aufbaut.**

**MVP Build:**
- Modul 1: Wissensartikel -- Zuerst bauen, alles haengt von Inhalten ab
- Modul 2: AI-Suche -- Einbinden, sobald Artikel existieren
- Modul 3: FAQ -- Spezieller Artikeltyp, schneller Erfolg (Quick Win)
- Modul 4: Benachrichtigungen -- Leichtgewichtig, hoher Impact
- Modul 5: Analytik -- Von Tag eins tracken, Dashboard spaeter

**V2 Build:**
- Fehlerbehebungsablaeufe und interaktive Checklisten
- Bus-Faktor-Dashboard
- Onboarding-Pfade
- Massenimport aus Loop / Z:-Laufwerk

**V3 Build:**
- Externe Kunden-Knowledge-Base
- In-App-Hilfe fuer psychodat
- Visuelle Anleitungen und Videos

---

## Folie 16 -- Offene Fragen und naechste Schritte

**Folgende Punkte muessen im Rahmen des Kickoff geklaert werden.**

- **Content-Typen (MVP):** Exakte Liste der Inhaltstypen und Formate (Inputs), die in die Knowledge Base aufgenommen werden (fuer die MVP-Version)
- **Dokument-Formate:** Welche Dokumente muessen gespeichert werden? Input: Welches Dokument (PDF/Excel/MP4) -- Anbindung an eine API, die transkribiert -- damit verbundene Kosten; Output: Definieren
- **MVP-Umfang:** Die finale Liste der im MVP enthaltenen Elemente muss festgelegt werden
- **Tech-Stack:** Finale Abstimmung
- **Daten-Upload:** Wie werden die Daten hochgeladen? Wer fuehrt es durch? Deadline?
- **Daten-Retrieval:** Vektor-Datenbank fuer AI-indexierten Zugriff -- Umsetzung in Supabase auf Frankfurter Servern

---

## Folie 17 -- Priorisierungslegende

**Uebersicht der Priorisierungsstufen ueber alle User Stories hinweg.**

| Stufe | Bedeutung |
|-------|-----------|
| MVP | Im initialen Release enthalten -- adressiert die kritischsten Pain Points |
| V2 | Zweite Iteration (nach Go-Live) -- Erweiterungen basierend auf Stakeholder-Input |
| V3 | Strategischer Langzeit-Plan -- kundenorientierte Funktionalitaet (Fabians Vision) |

---

*Ergosoft x Asuno -- Kickoff Workshop -- Februar 2026*
