# Hey Pizza · Madrid — Studio di localizzazione

Pagina web interattiva (un solo file `index.html`, nessuna dipendenza esterna oltre ai Google Fonts):
parallax, pizzaiolo animato, mappa di Madrid con strade OpenStreetMap e confini ufficiali dei 21 distretti,
sei locali in affitto con schede, pro/contro e link agli annunci Idealista (ricerca del 18/09/2026).

## Pubblicare

### Opzione A — GitHub Pages (gratis, HTTPS)
1. Settings → Pages → Source: `Deploy from a branch` → branch `main`, cartella `/ (root)`.
2. La pagina sarà su `https://cuoreneromarketing.github.io/heypizza-madrid/`.

### Opzione B — VPS con dominio nip.io
`nip.io` trasforma qualsiasi IP in un nome host senza registrare un dominio: `http://46.202.173.128.nip.io`
oppure `https://heypizza.46.202.173.128.nip.io`. Sul VPS (Docker):

```bash
git clone https://github.com/cuoreneromarketing/heypizza-madrid.git /opt/heypizza && cd /opt/heypizza
echo SITE_HOST=heypizza.46.202.173.128.nip.io > .env
docker compose up -d
```

## Fonti
- Distretti: dataset ufficiale dei distretti di Madrid (GeoJSON).
- Strade: OpenStreetMap (© OpenStreetMap contributors, ODbL).
- Annunci: Idealista, 18 settembre 2026. I dati possono cambiare rapidamente.
