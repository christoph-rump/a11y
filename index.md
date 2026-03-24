---
title: AI‑supported Accessibility Testing
---

# AI‑supported Accessibility Testing  
**Swiss Testing Day – Workshop Resources**

This page contains **public resources** from the Swiss Testing Day workshop  
*“AI‑supported Accessibility Testing”*.

It includes:
- Curated links to **semi‑automated accessibility tools**
- **Reusable LLM prompts** for accessibility testing
- Guidance on **responsible and realistic usage**

> ✅ All content is intentionally public and can be reused after the conference.

---

## 1. Semi‑automated Accessibility Tools

> ⚠️ These tools **support** accessibility testing – they do **not replace** manual testing or user testing.

### Browser‑based / Developer Tools
- **axe DevTools**  
  https://www.deque.com/axe/devtools/

- **Lighthouse (Chrome DevTools)**  
  https://developer.chrome.com/docs/lighthouse/

- **ARC Toolkit**  
  https://www.tpgi.com/arc-platform/arc-toolkit/

- **WAVE Evaluation Tool**  
  https://wave.webaim.org/

### Screen Readers (for validation)
- **NVDA (Windows, free)**  
  https://www.nvaccess.org/

- **VoiceOver (macOS / iOS, built‑in)**  
  https://support.apple.com/guide/voiceover/welcome/mac

---

## 2. LLM Prompt Library

> 🧠 These prompts are **starting points**.  
> Always validate results manually and with assistive technologies.

---

### WCAG 1.1.1 – Non‑text Content

```text
You are an accessibility testing expert.

Analyze the following HTML and identify potential violations of
WCAG 2.2 – Success Criterion 1.1.1 (Non‑text Content).

For each issue:
- Explain why it is an accessibility problem
- Describe the user impact
- Suggest an accessible alternative

HTML:
<PASTE HTML HERE>
