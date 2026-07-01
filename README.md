# Mapa GAL — Projecte

Aquest projecte conté un mapa interactiu basat en Leaflet que mostra les àrees dels Grups d'Acció Local (GAL) de Catalunya.

**Fitxers principals**

- [index.html](index.html) — pàgina principal del mapa.
- [codi_html.html](codi_html.html) — iframe d'exemple per incrustar el mapa.
- [gal_data.geojson](gal_data.geojson) — dades GeoJSON amb les geometries i propietats dels GALP.

**Requeriments**

Només cal un navegador modern i un servidor estàtic per evitar problemes de CORS quan es carreguen fitxers localment.

**Visualització local (mètode recomanat)**

Amb Python 3 instal·lat, obre un terminal a la carpeta i executa:

```bash
python -m http.server 8000
```

A continuació, obre `http://localhost:8000/index.html` al navegador.

Alternatives:

- Node.js: `npx http-server -p 8000` (requereix `http-server`).
- Extensió VS Code: Live Server.

**Com funciona**

- El mapa es crea a `index.html` utilitzant Leaflet.
- Les dades GeoJSON es carreguen amb `fetch('galp_data.geojson')` i es bandejen en una capa `L.geoJSON`.
- Estils i popups es defineixen dins de `index.html`.

**Notes i recomanacions**

- Si vols afegir una segona capa (per exemple `gal_data.geojson`), actualitza `index.html` per carregar-la i ajusta `totalLayers` perquè reflecteixi el nombre de capes carregades.
- Si el mapa no apareix, obre la consola del navegador (F12) per veure errors de CORS o rutes incorrectes.
- Pots optimitzar `galp_data.geojson` reduint la precisió de les coordenades amb eines com `mapshaper` si el fitxer és molt gran.

**Llicència i dades**

Comprova la llicència de les dades originals si les vols reutilitzar; el fitxer `galp_data.geojson` pot contenir metadades sobre la font.

**Contacte**

Per més informació habitate@arca-dr.cat

