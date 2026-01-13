# Silberhochzeit Webseite — Bereitstellung auf GitHub Pages

Diese Repository enthält die Datei `Silberhochzeit.html` und die zugehörigen Ressourcen.

Was ich hinzugefügt habe:

- `index.html` — Weiterleitung zur `Silberhochzeit.html` (damit die Seite unter der Root-URL erreichbar ist).
- `.github/workflows/gh-pages.yml` — GitHub Actions Workflow, der bei einem Push auf `main` oder `master` automatisch die Inhalte auf den `gh-pages` Branch veröffentlicht.

Wie Sie die Seite online stellen:

1. Erstelle ein Git-Repository, falls noch nicht vorhanden, und committe die Dateien:

```powershell
git init
git add .
git commit -m "Initial: add site and GitHub Pages workflow"
```

2. Erstelle ein Remote-Repository auf GitHub und verbinde es (ersetze `<REMOTE_URL>`):

```powershell
git remote add origin <REMOTE_URL>
git branch -M main
git push -u origin main
```

3. Nach dem Push wird der Workflow automatisch laufen und den Inhalt auf den Branch `gh-pages` deployen. GitHub Pages wird dann unter der URL
`https://<your-username>.github.io/<repo-name>/` erreichbar sein.

Hinweise:
- Wenn Sie eine benutzerdefinierte Domain nutzen möchten, fügen Sie eine `CNAME`-Datei in das Repository-Root ein.
- Falls Ihre Haupt-Branch nicht `main` heißt, passen Sie `.github/workflows/gh-pages.yml` an oder pushen auf `master`.
