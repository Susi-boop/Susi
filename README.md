# Livion Website

Schlichte, schwarz-weiße Produktseite für Livion. Reine statische Website
(HTML/CSS/JS) — läuft direkt auf GitHub Pages, kein Server nötig.

## Neues Produkt hinzufügen

1. Datei `products.js` öffnen.
2. Ein neues Objekt in die Liste kopieren und ausfüllen (Beispiel steht
   als Kommentar am Ende der Datei).
3. Änderung committen und pushen:
   ```bash
   git add products.js
   git commit -m "Neues Produkt hinzufügen"
   git push
   ```
4. GitHub Pages aktualisiert die Seite automatisch nach kurzer Zeit.

Es muss nichts am HTML, CSS oder JavaScript geändert werden — die
Produktkarten und die Detailansicht werden automatisch aus `products.js`
erzeugt.

## Auf GitHub Pages veröffentlichen

1. Alle Dateien (`index.html`, `style.css`, `script.js`, `products.js`)
   in ein GitHub-Repository legen.
2. Im Repo unter **Settings → Pages** als Quelle den `main`-Branch
   (Ordner `/root`) auswählen.
3. GitHub zeigt danach die URL an, unter der die Seite erreichbar ist
   (z. B. `https://<username>.github.io/<repo-name>/`).

## Grenzen dieser Lösung

- Es gibt keine Datenbank und kein Login — Produkte werden per Datei
  (`products.js`) im Code gepflegt, nicht über ein Formular auf der Seite.
- Für ein Formular, über das auch Nicht-Techniker ohne Git Produkte
  pflegen können, wäre ein externer Dienst nötig (z. B. Firebase,
  Supabase) — das ist mit reinem GitHub Pages nicht möglich.

## Struktur

```
index.html    Seitenstruktur
style.css     Design (schwarz/weiß, minimal)
script.js     Rendert Produkte, steuert die Detailansicht
products.js   Produktdaten — hier werden neue Produkte eingetragen
```
