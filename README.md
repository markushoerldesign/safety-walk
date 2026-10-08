# Safety Walk – Deployment (Vercel)

Inhalt: `index.html` (Seite), `api/chat.js` (KI-Funktion), Lebenslauf-PDF, Impressum, Datenschutz.

## 1. Vorbereiten
- `impressum.html`: Adresse ergänzen.
- Optional in `index.html` (Block CONFIG): `linkedin`, `letterUrl` eintragen.
- Neues Lebenslauf-PDF: Datei mit gleichem Namen ersetzen.

## 2. KI-Schlüssel
- console.anthropic.com → API Key erstellen, Guthaben aufladen, unter Billing ein monatliches Limit setzen (z. B. 5 €).

## 3. Auf Vercel veröffentlichen
1. Ordner in ein GitHub-Repository hochladen (oder `npx vercel` im Ordner ausführen).
2. vercel.com → Add New → Project → Repository wählen → Framework "Other" → Deploy.
3. Project → Settings → Environment Variables: `ANTHROPIC_API_KEY` = dein Key (optional `ANTHROPIC_MODEL`). Danach "Redeploy".

## 4. Subdomain safety.markushoerl.at
1. Vercel → Project → Settings → Domains → `safety.markushoerl.at` hinzufügen.
2. Beim DNS-Anbieter von markushoerl.at einen CNAME-Eintrag setzen: Name `safety`, Wert `cname.vercel-dns.com` (Vercel zeigt den genauen Wert an).
3. Nach wenigen Minuten ist die Seite mit HTTPS erreichbar. Danach QR-Code auf diese URL erzeugen.

## 5. Testen
Handy: Hotspots, CV-Download, Chat-Fragen (auch eine themenfremde), Kontakt-Button.
