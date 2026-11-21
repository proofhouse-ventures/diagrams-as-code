# Diagrams as Code for Confluence

Render **Mermaid**, **Graphviz (DOT)** and **PlantUML** diagrams from source
text, directly inside Confluence pages. Everything renders in the reader's
browser, inside Atlassian — the app declares no network egress, calls no
external service, and collects no data.

Published by **Proofhouse Ventures Pte. Ltd.** on the Atlassian Marketplace.
Support: wrenshelf@gmail.com (business days, Singapore time; best-effort
response within 2 business days).
Privacy policy: https://github.com/proofhouse-ventures/policies/blob/main/diagrams-as-code-privacy.md

## Getting started

1. Edit a Confluence page and insert the **Diagrams as Code** macro.
2. Pick a diagram type — or leave **Auto-detect** on; the macro recognises
   Mermaid, Graphviz and PlantUML sources automatically.
3. Paste or type your diagram source. The live preview renders as you type
   and flags syntax errors before you save.
4. Save. The diagram renders in the page for every reader, and the source
   stays in the page, versioned with your documentation.

Each diagram type ships a one-click sample in the editor so you can start
from a working example.

## Examples

Mermaid flowchart:

    flowchart TD
      A[Start] --> B{Decision}
      B -->|Yes| C[Ship it]
      B -->|No| D[Fix it]

Graphviz:

    digraph G {
      Web -> API
      API -> DB
    }

PlantUML:

    @startuml
    Alice -> Bob: Hello
    Bob --> Alice: Hi there
    @enduml

## Free vs Pro

**Free** (never expires, no diagram limit):

- Render Mermaid, Graphviz and PlantUML diagrams in pages
- Live preview with syntax validation while editing
- Default theme per engine

**Pro** (paid via Atlassian, per user per month):

- Extra themes — Mermaid: dark, forest, neutral · Graphviz: dark,
  blueprint, sepia · PlantUML: dark mode
- Export any rendered diagram as **SVG**, **PNG** or **PDF**
- Per-space diagram library: save diagrams under a title, preview them,
  reuse their source in any page, and delete entries you no longer need

## The diagram library (Pro)

From any rendered diagram, choose **Save to library** and give the entry a
title. Open **Diagram library** on any diagram in the same space to browse
saved entries, preview them, or delete them. In the macro editor, the
library section lists the same entries and **Use source** loads an entry's
source, type and theme into the editor.

Library entries are stored in Atlassian Forge hosted storage, under your
site and keyed by space.

## Privacy and security

- Diagram source is stored in the Confluence page's macro configuration;
  Pro library entries are stored in Forge hosted storage (Atlassian).
- The app requests only the `storage:app` permission. It makes no
  Confluence API calls and reads no page content or user data.
- No network egress, no external services, no analytics, no tracking, no
  sub-processors. Rendering is fully client-side from bundled libraries.
- PlantUML remote `!include` URLs are rejected by design, to preserve the
  no-egress guarantee.

Full privacy policy:
https://github.com/proofhouse-ventures/policies/blob/main/diagrams-as-code-privacy.md
