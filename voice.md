# Voice & Writing Standards

All prose generated for this repository -- in Markdown source files, HTML deliverables, and .docx outputs -- must follow these standards.

---

## No Em Dashes

Em dashes (U+2014, —) are prohibited in all documents. Replace them according to these rules:

- **Parenthetical aside:** use a comma pair or parentheses.
  - Before: `the chatbot project — the primary scope — returned 104 failures`
  - After: `the chatbot project (the primary scope) returned 104 failures`
- **List-style clarifier after a term:** use a colon.
  - Before: `Dialogflow CX — conversation engine for the chatbot`
  - After: `Dialogflow CX: conversation engine for the chatbot`
- **Sentence continuation or elaboration:** rewrite as a new sentence or use a comma.
  - Before: `there is no record of it — and no alert generated`
  - After: `there is no record of it, and no alert is generated`
- **Status key separators in tables:** use a pipe `|` or rewrite as a key-value pair.

Never substitute an en dash (U+2013) for an em dash. Use hyphens only for compound adjectives.

---

## Prose Rhythm and Register

Write for a technically literate human reader, not for a parser. The following influences define the target register.

**Toni Morrison, Haruki Murakami, Vernor Vinge (prose rhythm):**
- Sentences earn their length. A short sentence after a long one is deliberate, not accidental.
- Name things directly. Avoid nominalizations that bury the verb: not "the implementation of controls" but "implementing controls."
- Precision is not dryness. Technical accuracy and readable prose are not in conflict.
- Do not write around a fact. State it plainly, then explain its consequence.

**Martin Fowler, Gene Kim (systems thinking and architecture):**
- Every finding has a cause, an effect, and a path forward. Do not describe a problem without naming what it enables or prevents.
- Describe the system's current state before prescribing change. Readers trust a diagnosis before they trust a recommendation.
- Privileged access, audit visibility, and credential hygiene are not compliance checkboxes. They are properties of system behavior. Write them that way.
- Use concrete specifics: named service accounts, actual key ages in days, exact project counts. General statements erode credibility.

**IIT-style technical writing (precision and structure):**
- Documents have a hierarchy. Readers should be able to read only the headings and understand the shape of the argument.
- A table is a claim. Every row asserts a relationship. Do not include a row whose content does not justify its presence.
- Passive voice is acceptable when the actor is unknown or irrelevant. It is not acceptable when it obscures who is responsible.

---

## W3C and Human-Readability Standards

All client-facing HTML must be valid, semantic HTML5:
- Use `<main>`, `<section>`, `<article>`, `<header>`, `<footer>` as structural elements.
- All images must have `alt` text.
- Color alone must not convey meaning. Status badges must include text labels in addition to color.
- Minimum contrast ratio: 4.5:1 for body text (WCAG AA).
- Tables must use `<thead>`, `<tbody>`, and `<th scope="col">` for column headers.
- `lang="en"` must be set on the root `<html>` element.
- Font size must not drop below 12px in any rendered output.

---

## What to Avoid

- Filler openers: "This document provides...", "The purpose of this report is..."
- Hedging phrases: "it is worth noting that", "it should be mentioned that"
- Inflated urgency: "extremely critical", "very serious" -- if it is critical, name the specific consequence.
- Redundant intensity markers: "immediately urgent", "clearly obvious"
- Em dashes used for dramatic effect. State the drama plainly instead.
- Internal process disclosure in client-facing prose. Do not surface the verification steps, tooling, or internal methodology used to arrive at a conclusion. State the conclusion and its consequence.
  - Before: "I ran access verification checks today and confirmed that our Terraform automation account and my user have no org-level IAM."
  - After: "To move forward, we need the following IAM grants."
  - Before: "I matched each access error to the official GCP Cloud NGFW IAM documentation."
  - After: "These are the minimum roles per the GCP Cloud NGFW documentation."
  - The work happened. The client does not need to read about the work. They need to read what it produced.
