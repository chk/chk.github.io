# chk.github.io

Persönliche Website mit Blog, gebaut mit [Hugo](https://gohugo.io/) (Theme: [PaperMod](https://github.com/adityatelange/hugo-PaperMod)) und gehostet auf GitHub Pages.

## Inhalte schreiben

**Blog-Eintrag:** neue Datei in `content/posts/`, z. B. per

```bash
hugo new content posts/mein-titel.md
```

```markdown
---
title: "Mein Titel"
date: 2026-11-18T12:00:00+01:00
tags: ["thema"]
draft: false
---

Text in Markdown …
```

Einträge mit `draft: true` werden nicht veröffentlicht.

**Weitere Seite:** neue `.md`-Datei direkt in `content/`, z. B. `content/projekte.md`:

```markdown
---
title: "Projekte"
url: "/projekte/"
---
```

Damit sie in der Navigation erscheint, einen Eintrag unter `[menu]` in `hugo.toml` ergänzen.

## Deployment

Jeder Push auf `main` startet den Workflow `.github/workflows/pages.yml`, der die Seite baut und auf GitHub Pages veröffentlicht. Unter *Actions* lässt er sich auch manuell starten.

Einmalig nötig: unter *Settings → Pages → Build and deployment* als *Source* **GitHub Actions** auswählen.

## Lokal ansehen

```bash
git submodule update --init   # nach dem Klonen: Theme laden
hugo server -D                # -D zeigt auch Entwürfe
```

Danach unter http://localhost:1313 öffnen.
