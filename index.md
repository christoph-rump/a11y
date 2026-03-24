---
title: Swiss Testing Day 2026 – KI als Ansatz von Barrierefreiheits‑Tests – Workshop
---

# Swiss Testing Day 2026 – KI als Ansatz von Barrierefreiheits‑Tests  
**Workshop – Conference Resources**

Diese Seite enthält **öffentliche Workshop‑Ressourcen** vom  
**Swiss Testing Day 2026** zum Thema:

**„KI als Ansatz von Barrierefreiheits‑Tests“**

Enthalten sind:
- Kuratierte Links zu **semi‑automatisierten Barrierefreiheits‑Tools**
- **Wiederverwendbare LLM‑Prompts** für Accessibility‑Tests
- Hinweise zu **Grenzen, Risiken und verantwortungsvollem Einsatz**

> ✅ Alle Inhalte sind bewusst **öffentlich** und auch **nach der Konferenz** nutzbar.

---

## 1. Semi‑automatisierte Barrierefreiheits‑Tools

> ⚠️ Diese Tools **unterstützen** Barrierefreiheits‑Tests,  
> ersetzen jedoch **keine manuellen Tests** oder Tests mit Assistive Technologies.

### Browser‑Erweiterungen & Developer‑Tools

- **WAVE – Web Accessibility Evaluation Tool**  
  (Browser‑Extension für Chrome, Edge, Firefox)  
  👉 https://wave.webaim.org/

- **axe DevTools (Browser Extension)**  
  👉 https://www.deque.com/axe/devtools/

- **ARC Toolkit (Browser Extension)**  
  👉 https://www.tpgi.com/arc-platform/arc-toolkit/

- **Lighthouse (Chrome DevTools)**  
  👉 https://developer.chrome.com/docs/lighthouse/

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

### WCAG 1.1.1 – Nicht‑Text‑Inhalte

```text
Du bist Expert:in für digitale Barrierefreiheit.

Analysiere den folgenden HTML‑Code im Hinblick auf
WCAG 2.2 – Erfolgskriterium 1.1.1 (Nicht‑Text‑Inhalte).

Für jedes identifizierte Problem:
- Erkläre, warum es ein Barrierefreiheitsproblem ist
- Beschreibe die Auswirkung auf Nutzer:innen
- Schlage eine barrierefreie Alternative vor

HTML:
<HIER HTML EINFÜGEN>
