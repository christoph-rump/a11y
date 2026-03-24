---
title: Swiss Testing Day 2026 – KI als Ansatz zur Reduktion von aufwändigen Barrierefreiheits-Tests – Workshop
---

# Swiss Testing Day 2026 – KI als Ansatz zur Reduktion von aufwändigen Barrierefreiheits-Tests

Diese Seite enthält **öffentliche Materialien** zu dem Workshop mit dem Titel **„KI als Ansatz von Barrierefreiheits‑Tests“**

Enthalten sind:
- Eine Auswahl an Links zu **semi-automatisierten und automatisierten Barrierefreiheits‑Tools**
- **Wiederverwendbare LLM‑Prompts** für Barrierefreiheits-Tests
- Hinweise zu **Grenzen, Risiken und verantwortungsvollem Einsatz**

> ✅ Alle Inhalte sind bewusst **öffentlich** und auch **nach der Konferenz** nutzbar.

---

## Web Content Accessibility Guidelines (WCAG)

- **WCAG Version 2.1**
  https://www.w3.org/TR/WCAG21/
- **WCAG Version 2.2**
  https://www.w3.org/TR/WCAG22/

---

## 1. Barrierefreiheits‑Test Tools

> ⚠️ Diese Tools **unterstützen** Barrierefreiheits‑Tests,  
> ersetzen jedoch **keine manuellen Tests** oder Tests mit Assistive Technologies.

### Browser‑Erweiterungen & Developer‑Tools

- **WAVE – Web Accessibility Evaluation Tool**  
  (Browser‑Extension für Chrome, Edge, Firefox)  
  https://wave.webaim.org/extension/

- **axe-core (Open Source Library)**
  https://www.deque.com/axe/axe-core/

- **axe DevTools (Lizenz)**  
  https://www.deque.com/axe/devtools/

- **Lighthouse (Chrome DevTools)**  
  https://developer.chrome.com/docs/lighthouse/


> 🔎 **Hinweis:**  
> Auch bei Browser‑Extensions gilt: Ergebnisse **immer manuell validieren**.


### Screenreader (für manuelle Validierung)

- **NVDA (Windows, kostenlos)**  
  https://www.nvaccess.org/

- **VoiceOver (macOS / iOS, integriert)**  
  https://support.apple.com/guide/voiceover/welcome/mac

---

## 2. LLM‑Prompt‑Bibliothek

> 🧠 Die folgenden Prompts sind **Startpunkte**.  
> Ergebnisse müssen immer **fachlich geprüft** und **manuell verifiziert** werden.

---

### Prompt-Blueprint

**Rolle:** Accessibility Expert*in für WCAG2.1 Kriterium 3.3.2 […]

**Ziel:** Sicherstellen, dass alle Steuerelemente klar verständliche Instruktionen und Text darbieten […]

**Aufgabe:** Analysiere die Webseite mit URL [einfügen] zu Kriterium 3.3.2 mit folgenden Prüfschritten […]

**Anforderungen:** Prüfe nur Kriterium 3.3.2 und nicht 1.3.1 oder 4.1.2, gib eine Begründung ab

**Einschränkungen:** Strukturiere die Antwort in einer einzigen Tabelle mit folgenden Spalten […]

**Format/Stil:** Analytisch, präzise

**Scope:** Fokussiere dich auf Klarheit der Anweisungen, exkludiere Design, Layout und Code Empfehlungen

**Kritische Selbsteinschätzung:** Überprüfe die Ergebnisse anhand des Prompts kritisch, vor Darstellung des finalen Ergebnisses

---

### WCAG 3.1.1 – Sprache einer Webseite

Role: Accessibility Expert specializing in WCAG 2.1 Success Criterion  3.1.1 Language of Page, internationalization best practices, and assistive‑technology‑friendly language configuration.

Goal: Ensure that the page’s default human language is correctly identified, programmatically determinable, and supports accurate pronunciation, rendering, and comprehension for all users and assistive technologies.

Task:
Analyze the webpage at: [insert URL]
Focus exclusively on WCAG 2.1 SC 3.1.1 Language of Page.
•	Analyze whether the webpage correctly defines its default language.
•	Identify missing, incorrect, or non‑standard lang attributes.
•	Check whether the declared language matches the predominant content language.
•	Detect invalid, ambiguous, or misapplied language codes.
•	Suggest concise, correct language attribute values using valid IETF BCP‑47 codes.
•	Verify that the primary language can be programmatically determined.
•	If discrepancies exist between declared and actual language, propose a corrected lang value.

Requirements:
•	Only analyze the page-level language declaration (not inline language changes).
•	Review the actual page content to verify which language is predominant.

Constraints:
Your entire response must consist only of one single Markdown table with the following columns:
| Element / Context | Current State | Issue | Suggested Fix | Explanation / Rationale | Audience Impact |

Style: plain, analytical, concise.
Scope: language determinability and correctness; exclude design/layout/code suggestions unrelated to SC 3.1.1.
Self-check: Verify all constraints before final answer.

---

### WCAG 3.2.2 – Labels oder Instructions

Role: Accessibility Expert specializing in WCAG 2.1 Success Criterion  3.3.2 Labels or Instructions, cognitive‑accessibility best practices, and form‑interaction clarity.

Goal: Ensure that all form controls and user‑input elements provide clear, visible, and understandable labels or instructions so users know what information is required and how to enter it.

Task:
Analyze the webpage at: [insert URL]
Focus exclusively on WCAG 2.1 SC 3.3.2 Labels or Instructions.
•	Identify all input fields, controls, and form elements that require user input.
•	Check whether each input provides a visible and understandable label.
•	Identify missing, unclear, ambiguous, or overly minimal labels.
•	Detect missing instructions when specific formats, rules, or constraints apply (e.g., date formats, password rules).
•	Identify cases where labels exist programmatically but are not visible to all users, which fails SC 3.3.2.
•	Suggest concise, clear labels or instructions that improve understanding.
•	Evaluate whether image‑based labels are understandable or need additional text support.
•	Propose corrected or enhanced labels/instructions where necessary.

Requirements:
•	Only analyze labels and instructions for user‑input fields, not their programmatic association (covered by SC 1.3.1 and SC 4.1.2).
•	Review the actual visual presentation to verify that labels are visible, clear, and sufficiently descriptive.

Constraints:
Your entire response must consist only of one single Markdown table with the following columns:

| Input / Context | Current State | Issue | Suggested Fix | Explanation / Rationale | Audience Impact |

Style: plain, analytical, concise.
Scope: label clarity and instruction sufficiency; exclude design/layout/code suggestions unrelated to SC 3.3.2.
Self-check: Verify all constraints before final answer.
