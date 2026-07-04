# ARDE Portafolio Web (sin precios)

Página dedicada de ARDE — todo el portafolio del PDF convertido en web:
identidad, problema/solución, manifiesto, pilares, 9 films con video real,
4 casos de branding, AI Smart Content, 6 servicios, comparativa AI vs
tradicional y CTA. **Sin precios** (a diferencia de arde-producciones).

## Deploy (GitHub Pages, igual que arde-producciones)
```bash
cd ~/Documents/arde_portafolio_page
git init && git add -A && git commit -m "ARDE portafolio web 2026"
# crear repo "arde-portafolio" en la org Ardeagency y push
git remote add origin git@github.com:Ardeagency/arde-portafolio.git
git branch -M main && git push -u origin main
# Activar GitHub Pages: Settings → Pages → main / root
```
URL final: **https://ardeagency.github.io/arde-portafolio/**
(La cotización de La Costeña ya apunta a esa URL en sus 2 botones de portafolio.)

## Peso
- Imágenes: ~10 MB (páginas del PDF + galerías por proyecto en assets/img/gal/)
- Videos: ~170 MB. Los players usan `preload="none"` (descargan al dar play);
  los loops (BODYARMOR, reels Saúl, film AI Smart Content) usan `preload="metadata"`.
  GitHub Pages lo soporta (límite blando 1 GB por repo).

## Preview local
Los videos necesitan un servidor con range requests:
`python3 /tmp/range_server2.py` → http://localhost:8778/
