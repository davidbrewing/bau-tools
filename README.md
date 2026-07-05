# Bau-Tools – Anleitung zum Online-Stellen

Dieser Ordner enthält drei Dateien:

- `index.html` – kleine Startseite mit Links zu beiden Tools
- `umbau-machbarkeitscheck.html` – Prototyp 1 (Industrie/Bestand)
- `bauvorhaben-regel-check.html` – Prototyp 2 (Privat/Zuhause)

Das sind reine HTML/CSS/JavaScript-Dateien ohne Server im Hintergrund ("statische Website"). Genau deshalb ist das Online-Stellen sehr einfach – es gibt keine Datenbank und keinen Programmcode, der irgendwo installiert werden müsste.

## Weg 1: In 2 Minuten testen (ohne Account)

1. Gehe im Browser auf **app.netlify.com/drop**
2. Ziehe den kompletten Ordner (oder die drei Dateien) per Drag & Drop in das Browserfenster
3. Netlify gibt dir sofort eine öffentliche Adresse (z. B. `https://irgendwas-123.netlify.app`), die du mit anderen teilen kannst

Nachteil: Ohne kostenlosen Account verschwindet die Seite nach einer Weile wieder bzw. lässt sich nicht aktualisieren. Für einen schnellen Test an Kollegen/Freunden reicht das trotzdem aus.

## Weg 2: Dauerhaft, mit eigenem Account (empfohlen)

Das ist der Weg, den man auch für spätere, größere Projekte weiterverwenden kann.

1. **Kostenlosen GitHub-Account erstellen**: github.com → Sign up
2. **Neues Repository anlegen** (z. B. "bau-tools"), öffentlich oder privat, ohne weitere Vorlagen
3. Die drei Dateien aus diesem Ordner in das Repository hochladen (auf GitHub: "Add file" → "Upload files", Dateien reinziehen, "Commit changes")
4. **Kostenlosen Netlify- oder Vercel-Account erstellen** und mit dem GitHub-Account verbinden
5. Dort "Neue Seite/Projekt importieren" wählen und das gerade angelegte Repository auswählen
6. Da es sich um eine reine HTML-Seite handelt, sind keine Build-Einstellungen nötig – einfach übernehmen und deployen lassen
7. Du bekommst eine feste, öffentliche Adresse. Jede Änderung, die du später auf GitHub hochlädst, wird automatisch neu veröffentlicht

## Eigene Domain (optional)

Wenn du später eine eigene Adresse willst (z. B. `www.dein-name.de`):

1. Domain bei einem Anbieter registrieren (z. B. IONOS, Namecheap, Cloudflare) – meist 8–15 €/Jahr
2. In den Domain-Einstellungen die DNS-Einträge auf Netlify/Vercel zeigen lassen (die zeigen dir in ihren Einstellungen genau, welche Einträge nötig sind)
3. Netlify/Vercel richtet dafür automatisch ein kostenloses SSL-Zertifikat (https) ein

## Wichtig zu wissen

Beide Tools laufen komplett im Browser des Nutzers – es werden aktuell keine Daten irgendwo gespeichert oder an dich übermittelt. Das ist für einen ersten Test gut (keine Datenschutzfragen), heißt aber auch: du siehst nicht, wie viele Leute das Tool nutzen oder was sie eingeben.

Für den nächsten Schritt (z. B. E-Mail-Adressen für eine Warteliste sammeln, oder später die Vermittlung an Tragwerksplaner) reicht die aktuelle statische Seite nicht mehr aus – dafür braucht es einen kleinen Zusatzbaustein wie Formspree oder Tally (für einfache Formulare, ohne eigenen Code) oder später Supabase/Firebase (wenn mehr Logik dazukommt). Das ist aber erst relevant, wenn ihr über reines Testen hinausgeht.
