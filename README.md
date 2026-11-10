# Stundenplan Live auf Render

Dieses Projekt enthält die grafische App und den WebUntis-Proxy zusammen. Beide laufen auf derselben Render-Adresse; der Browser ruft die API same-origin auf. So umgehst du die fremde Domain, die in der Langdock-Vorschau durch CSP blockiert wurde.

## Render-Schritte

1. Lade den Inhalt dieses Ordners in ein neues GitHub-Repository.
2. In Render: New → Web Service und dieses Repository auswählen.
3. Runtime: Node; Root Directory leer lassen, wenn die Dateien im Repo-Hauptordner liegen.
4. Build Command: `npm install && npm run build`
5. Start Command: `npm start`
6. Deploy. Keine Zugangsdaten oder Environment-Variablen nötig.

Nach Deploy zeigt die Root-URL (`https://DEINE-APP.onrender.com/`) die Grafik-App. `/api/health` ist nur ein JSON-Gesundheitstest; `/api/webuntis/week?...` liefert absichtlich Roh-JSON.
