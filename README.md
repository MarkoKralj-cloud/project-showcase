# Project Showcase

Zwei KI-Produkte, die ich konzipiert, gestaltet und umgesetzt habe.
Dieses Repository enthält nur die Präsentation: Screenshots und Beschreibungen. Der Quellcode ist privat.

**Live-Seite:** https://markokralj-cloud.github.io/project-showcase/

---

## AI Inbox – KI-gestützter Kundensupport

Eingehende Support-E-Mails werden klassifiziert, mit der eigenen Wissensdatenbank abgeglichen und als Antwortentwurf vorbereitet. Ein Mensch prüft und gibt frei; Routinefälle können je Kategorie automatisch versendet werden.

![Fallansicht mit KI-Entwurf und Quellen](assets/ai-inbox/ticket-detail.webp)

**Ablauf:** Eingang → Klassifizierung → Wissenssuche (RAG) → Entwurf mit Konfidenz → Prüfung → Versand

- E-Mail-Eingang per IMAP, Versand per SMTP
- Klassifizierung nach Anliegen, Thema, Dringlichkeit und Stimmung
- Retrieval-Augmented Generation über Dokumente, URLs und Notion
- Antwortentwurf mit Konfidenzwert und nachvollziehbaren Quellen
- Freigabe-Workflow: menschliche Prüfung oder Auto-Versand je Kategorie
- Auswertung von Akzeptanzrate, Bearbeitungsrate und Wissenslücken
- Mehrmandantenfähig, mit Teamrollen, Audit-Log und Abrechnung

**Engineering-Schwerpunkte:** Ticket-Zustandsmaschine, Versandgarantie ohne Doppelzustellung, strikte Mandantentrennung, Logs ohne personenbezogene Daten, knapp 500 automatisierte Tests plus visuelle Regressionstests.

**Technik:** TypeScript · React · Vite · Tailwind CSS · Node.js/Express · PostgreSQL · OpenAI API · Clerk · Stripe · Sentry · Vitest · Playwright

| Start | KI-Leistung | Wissensdatenbank |
|---|---|---|
| ![Start](assets/ai-inbox/dashboard.webp) | ![KI-Leistung](assets/ai-inbox/analytics.webp) | ![Wissensdatenbank](assets/ai-inbox/knowledge.webp) |

---

## Content Planner – vom Video zum geplanten Post

Videos hochladen, transkribieren lassen und pro Plattform passende Captions und Hashtags erhalten. Die Posts werden im Kalender geplant, vor der Veröffentlichung gegen Plattformregeln geprüft und zum geplanten Zeitpunkt automatisch veröffentlicht.

![Wochenkalender mit geplanten Posts](assets/content-planner/dashboard-week.webp)

**Ablauf:** Upload → Transkript → KI-Caption → Planung → Preflight-Prüfung → Veröffentlichung

- Video-Upload in einen S3-kompatiblen Speicher
- Transkription und KI-Captions pro Plattform, mit Markenstimme und Hashtag-Pool
- Wochen- und Monatskalender mit Drag-and-drop und Zeitvorschlag aus Reichweitendaten
- Automatische Veröffentlichung: Instagram und Facebook über die Meta Graph API, TikTok und YouTube über einen Publishing-Dienst
- Preflight-Regelwerk mit 18 Plattformregeln gegen Reichweitenverlust
- Archiv veröffentlichter Inhalte, Fehler- und Wartungszustände

**Technik:** TypeScript · Next.js · React · Tailwind CSS · Drizzle ORM · PostgreSQL · Node.js Worker · OpenAI API · Whisper · S3 Storage · Meta Graph API · Clerk

| Editor | Monatsansicht | Mobil |
|---|---|---|
| ![Editor](assets/content-planner/draft-editor.webp) | ![Monat](assets/content-planner/dashboard-month.webp) | ![Mobil](assets/content-planner/mobile-dashboard.webp) |

---

## Arbeitsweise

Konzept, Produktdesign und Umsetzung beider Produkte. Entwickelt mit KI-Coding-Agents (Claude Code, Codex) nach festen Regeln: dokumentierte Invarianten, ein Branch pro Arbeitspaket, Lint, Typecheck und Tests vor jedem Commit, unabhängiges Review vor jedem Merge.

*Alle Screenshots zeigen lokale Demo-Umgebungen mit erfundenen Daten. Video- und Bildvorschauen sind Platzhalter.*
