# Osobní web — Tomáš Kyjovský

Jednostránkový osobní web (CV) postavený jako jeden statický soubor.

## Obsah
- `index.html` — celý web (HTML + CSS + JS v jednom souboru, žádné závislosti)
- `staticwebapp.config.json` — konfigurace pro Azure Static Web Apps

## Nasazení na Azure Static Web Apps (z lokálu, bez GitHubu)

1. V Azure Portálu vytvoř Static Web App s **Deployment source: Other**.
2. V Portálu → tvoje app → Overview → **Manage deployment token** → zkopíruj token.
3. V této složce spusť v terminálu:

   ```bash
   npm install -g @azure/static-web-apps-cli
   swa deploy ./ --deployment-token <TOKEN> --env production
   ```

Hotovo — web poběží na adrese `https://<nazev>.azurestaticapps.net`.

## Úpravy
Stačí editovat `index.html` a znovu spustit `swa deploy`.
