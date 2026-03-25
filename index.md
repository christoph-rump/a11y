---
lang: de
title: Swiss Testing Day 2026 – KI als Ansatz zur Reduktion von aufwändigen Barrierefreiheits-Tests – Workshop
---

# Swiss Testing Day 2026 – KI als Ansatz zur Reduktion von aufwändigen Barrierefreiheits-Tests

Diese Seite enthält **Materialien** zu dem Workshop mit dem Titel **„KI als Ansatz zur Reduktion von aufwändigen Barrierefreiheits-Tests“**

Enthalten sind:
- Eine Auswahl an Links zu **semi-automatisierten und automatisierten Barrierefreiheits‑Tools**
- **Wiederverwendbare LLM‑Prompts** für Barrierefreiheits-Tests

> 
> ✅ Alle Inhalte sind auch **nach der Konferenz** nutzbar.
<br>

---

## Web Content Accessibility Guidelines (WCAG)
 
- **WCAG Version 2.1**: 
  [Link zu WCAG 2.1 Spezifikation](https://www.w3.org/TR/WCAG21/)
- **WCAG Version 2.2**: 
  [Link zu WCAG 2.2 Spezifikation](https://www.w3.org/TR/WCAG22/)
<br><br>

---

## 1. Barrierefreiheits‑Test Tools
 
> ⚠️ Diese Tools **unterstützen** Barrierefreiheits‑Tests,  
> ersetzen jedoch **keine manuellen Tests** oder Tests mit assistiven Technologien.
> 

### Browser‑Erweiterungen & Developer‑Tools

- **WAVE – Web Accessibility Evaluation Tool**:
  [Link zu WAVE Browser Plugin für Chrome, Edge, Firefox](https://wave.webaim.org/extension/)
<br>
 
- **axe-core (Open Source Library)**: 
  [Link zu axe-core](https://www.deque.com/axe/axe-core/)
<br>
 
- **axe DevTools (Lizenz)**: 
  [Link zu axe DevTools](https://www.deque.com/axe/devtools/)
<br>
 
- **Lighthouse (Chrome DevTools)**:
  [Link zu Google Lighthouse Chrome Plugin](https://developer.chrome.com/docs/lighthouse/)
<br>
 
> 
> 🔎 **Hinweis:**  Auch bei Browser‑Extensions gilt: Ergebnisse **immer manuell validieren**.
> 

<br>
### Screenreader (für manuelle Validierung)

- **NVDA (Windows, kostenlos)** 
  [Link zu NVDA](https://www.nvaccess.org/)
 <br>

- **VoiceOver (macOS / iOS, integriert)**  
[Link zu VoiceOver](https://support.apple.com/guide/voiceover/welcome/mac)
<br>

- **TalkBack (Android, integriert)** 
- [Link zu Informationen zu TalkBack](https://support.google.com/accessibility/android/answer/6007100?hl%3Den)
<br>

<br> 
---

## 2. LLM‑Prompt‑Bibliothek 

> 
> 🧠 Die folgenden Prompts sind **Startpunkte**.  
> Ergebnisse müssen immer **fachlich geprüft** und **manuell verifiziert** werden.
> 

---

### 2.1 Prompt-Blueprint

**Rolle:** Die Rolle, die eingenommen werden soll, z.B. die einer Accessibility Expert*in für das WCAG 2.1 Kriterium 3.3.2.

**Ziel:** Beschreibt das generelle Ziel, idealerweise eine gute Beschreibung des Kriteriums, z.B. Sicherstellen, dass alle Steuerelemente klar verständliche Instruktionen und Text darbieten.

**Aufgabe:** Die eigentliche Aufgabe, d.h. die Analyse der Webseite mit der eingegebenen URL zu einem Kriterium mit einer Reihe von Prüfschritten.

**Anforderungen:** Konkretisiere die Prüfung hinsichtlich des Kriteriums. Z.B. nur Fokus auf Kriterium 3.3.2 und nicht ähnliche Kriterien, plus Abgabe einer Begründung.

**Einschränkungen:** Kann gut genutzt werden, um die Antwort einzuschränken, z.B. soll die Antwort in einer einzigen Tabelle mit folgenden Spalten strukturiert werden […].

**Format/Stil:** Welcher Stil soll ausgegeben werden, welcher "Ton", z.B. analytisch, sehr präzise.

**Scope:** Der Rahmen und Umfang, z.B. fokussiere dich auf Klarheit der Anweisungen, exkludiere Design, Layout und Code Empfehlungen.

**Kritische Selbsteinschätzung:** Überprüfe die Ergebnisse anhand des Prompts kritisch, vor Darstellung des finalen Ergebnisses.

---

### WCAG 3.1.1 – Language of Page

[Link zu WCAG Kriterium 3.1.1 auf der W3C Seite](https://www.w3.org/WAI/WCAG21/Understanding/language-of-page.html)

#### <ins>Prompt auf English</ins> 

**Role:** Accessibility Expert specializing in WCAG 2.1 Success Criterion  3.1.1 Language of Page, internationalization best practices, and assistive‑technology‑friendly language configuration.

**Goal:** Ensure that the page’s default human language is correctly identified, programmatically determinable, and supports accurate pronunciation, rendering, and comprehension for all users and assistive technologies.

**Task:**
- Analyze the webpage at: [insert URL]
- Focus exclusively on WCAG 2.1 SC 3.1.1 Language of Page.
- Analyze whether the webpage correctly defines its default language.
- Identify missing, incorrect, or non‑standard lang attributes.
- Check whether the declared language matches the predominant content language.
- Detect invalid, ambiguous, or misapplied language codes.
- Suggest concise, correct language attribute values using valid IETF BCP‑47 codes.
- Verify that the primary language can be programmatically determined.
- If discrepancies exist between declared and actual language, propose a corrected lang value.

**Requirements:**
- Only analyze the page-level language declaration (not inline language changes).
- Review the actual page content to verify which language is predominant.

**Constraints:** Your entire response must consist only of one single Markdown table with the following columns:
| Element / Context | Current State | Issue | Suggested Fix | Explanation / Rationale | Audience Impact |

**Style:** plain, analytical, concise.

**Scope:** language determinability and correctness; exclude design/layout/code suggestions unrelated to SC 3.1.1.

**Self-check:** Verify all constraints before final answer. 

<br> 

#### <ins>Prompt auf Deutsch</ins> 

**Rolle:** Accessibility Expert*in spezialisiert auf WCAG Version 2.1 und Erfolgskriterium 3.1.1 Sprache der Seite, Internationalisierungs Best Practices, und assistiver-Technologie-freundlicher Sprachkonfiguration. 

**Ziel:** Stelle sicher, dass die von der Webseite definierte Standard Sprache korrekt identifiziert wird, programmatisch bestimmt werden kann, und korrekte Aussprache unterstützt, mit Verständnis für alle Nutzer und assistive Technologien. 

**Aufgabe:**
- Analysiere die URL unter folgender URL [URL eingeben]
- Fokussiere dich ausschliesslich auf WCAG 2.1 Erfolgskriterium 3.1.1, Sprache der Seite.
- Analysiere, ob die Webseite ihre Standardsprache korrekt definiert.
- Identifiziere fehlende, inkorrekte, oder nicht-Standard lang Attribute.
- Prüfe, ob die deklarierte Sprache mit der vorrangig dominierten Inhaltssprache übereinstimmt.
- Erkenne invalide, mehrdeutige, or falsch angewendete Sprachcodes.
- Schlage genaue, korrekte Sprachattribut Werte vor, gemäss valider IETF BCP‑47 Codes.
- Verifiziere das die primäre Sprache programmatisch determiniert werden kann.
- Falls eine Diskrepanz besteht zwischen deklarierter und tatsächlicher Sprache, dann schlage den korrekten lang Wert vor.

**Anforderungen:** 
- Analysierte nur die Seitenlevel Sprach Deklaration (nicht mögliche Sprachwechsel).
- Review den eigentlichen Seiteninhalt um zu validieren welche Sprache predominant ist.

**Einschränkungen:** Deine gesamte Antwort darf nur aus einer einzelnen Markdown Tabelle mit folgenden Spalten bestehen:
| Element / Kontext | Aktueller Stand | Problem | Vorgeschlagene Änderung | Erläuterung | Auswirkung auf Endnutzer |

**Format/Stil:** Simpel, analytisch, prägnant. 

**Scope:** Bestimmung der Sprache und Korrektheit; exkludiere Design, Layout und Code Empfehlungen, sowie Empfehlungen abseits von Kriterium 3.1.1. 

**Kritische Selbsteinschätzung:** Verifiziere und validiere deine Analyse bevor du ein finales Ergebnis ausgibst.

<br> 

---

### WCAG 3.2.2 – Labels oder Instructions

[Link zu WCAG Kriterium 3.1.1 auf der W3C Seite](https://www.w3.org/WAI/WCAG21/Understanding/labels-or-instructions.html)

#### <ins>Prompt auf English</ins> 

**Role:** Accessibility Expert specializing in WCAG 2.1 Success Criterion  3.3.2 Labels or Instructions, cognitive‑accessibility best practices, and form‑interaction clarity.

**Goal:** Ensure that all form controls and user‑input elements provide clear, visible, and understandable labels or instructions so users know what information is required and how to enter it.

**Task:**
- Analyze the webpage at: [insert URL]
- Focus exclusively on WCAG 2.1 SC 3.3.2 Labels or Instructions.
- Identify all input fields, controls, and form elements that require user input.
- Check whether each input provides a visible and understandable label.
- Identify missing, unclear, ambiguous, or overly minimal labels.
- Detect missing instructions when specific formats, rules, or constraints apply (e.g., date formats, password rules).
- Identify cases where labels exist programmatically but are not visible to all users, which fails SC 3.3.2.
- Suggest concise, clear labels or instructions that improve understanding.
- Evaluate whether image‑based labels are understandable or need additional text support.
- Propose corrected or enhanced labels/instructions where necessary.

**Requirements:**
- Only analyze labels and instructions for user‑input fields, not their programmatic association (covered by SC 1.3.1 and SC 4.1.2).
- Review the actual visual presentation to verify that labels are visible, clear, and sufficiently descriptive.

**Constraints:** Your entire response must consist only of one single Markdown table with the following columns:
| Input / Context | Current State | Issue | Suggested Fix | Explanation / Rationale | Audience Impact |

**Style:** plain, analytical, concise.

**Scope:** label clarity and instruction sufficiency; exclude design/layout/code suggestions unrelated to SC 3.3.2.

**Self-check:** Verify all constraints before final answer.
 
<br> 

#### <ins>Prompt auf Deutsch</ins> 

**Rolle:** Accessibility Expert*in spezialisiert auf WCAG Version 2.1 und Erfolgskriterium 3.3.2 Labels und Instruktionen, kognitiven Barrierefreiheits Best Practices, und klarem Verständnis für Bedienelement Interaktionen. 

**Ziel:** Stelle sicher, dass alle Bedienelemente und Eingabeelemente klare, sichtbare und verständliche Labels oder Instruktionen vorweisen, so dass Nutzer wissen welche Informationen benötigt werden und wie diese einzugeben sind.

**Aufgabe:**
- Analysiere die URL unter folgender URL [URL eingeben]
- Fokussiere dich ausschliesslich auf WCAG 2.1 Erfolgskriterium 3.3.2, Labels oder Instruktionen.
- Identifiziere alle Eingabefelder, Bedienelemente und Formelemente die einen Nutzer Input benötigen.
- Prüfe, ob jeder benötigte Input ein sichtbares und verständliches Label vorweist.
- Identifiziere fehlende, unklare, mehrdeutige oder zu kurzen/minimalen Label.
- Erkenne fehlende Instruktionen, when spezifische Formate, Regeln oder Einschränkungen zutreffen (z.B. Datum Format, Passwort oder E-Mail Regeln).
- Identifiziere Fälle bei denen Label programmatisch existieren, aber nicht sichtbar für alle Nutzer sind, was das Kriterium 3.3.2 fehlschlägen lässt.
- Schlage prägnante, klare Labels oder Instruktionen vor, die das Verständnis verbessern.
- Evaluiere, ob Bild-basierte Labels verständlich sind oder zusätzliche Text Unterstützung benötigen.
- Schlage korrigierte oder verbesserte Labels und/oder Instruktionen vor, wo immer es nötig ist.

**Anforderungen:**
- Analysiere nur Labels und Instruktionen für Eingabefelder und Elemente, nicht die programmatische Assoziation (abgedeckt durch Kriterium 1.3.1 und 4.1.2).
- Review die tatsächliche visuelle Darstellung und verifiziere das Labels sichtbar sind, klar, und ausreichend beschrieben.

**Einschränkungen:** Deine gesamte Antwort darf nur aus einer einzelnen Markdown Tabelle mit folgenden Spalten bestehen:
| Element / Kontext | Aktueller Stand | Problem | Vorgeschlagene Änderung | Erläuterung | Auswirkung auf Endnutzer |

**Format/Stil:** Simpel, analytisch, prägnant. 

**Scope:** Klarheit der Labels und Instruktionen; exkludiere Design, Layout und Code Empfehlungen, sowie Empfehlungen abseits von Kriterium 3.3.2. 

**Kritische Selbsteinschätzung:** Verifiziere und validiere deine Analyse bevor du ein finales Ergebnis ausgibst.

<br> 
---

### 2.2 Aufgabe zum Prompting

Schreibe einen Prompt zu einem der beiden folgenden Themen und wende ihn auf eine von dir ausgewählte Webseite an 
- Auswirkung von fehlendem oder nicht geeignetem Alternativ-Text: WCAG Kriterium 1.1.1 Non-text Content [Link zu WCAG-Kriterium 1.1.1](https://www.w3.org/WAI/WCAG21/Understanding/non-text-content) oder zu 
- Auswirkungen von fehlendem oder nicht geeignetem Text bei Links und Buttons: WCAG Kriterium 2.4.4 Link Purpose [Link zu WCAG-Kriterium 2.4.4](https://www.w3.org/WAI/WCAG21/Understanding/link-purpose-in-context.html)

