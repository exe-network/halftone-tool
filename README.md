# exe Halftone Tool

Browser-Tool zum Rastern von Grafiken für DTF-Druck (Direct-to-Film). 100% client-side — keine Daten verlassen den Browser.

## Was es macht

Halftone-Rasterung wandelt weiche Übergänge (Glows, Schatten, Verläufe, halbtransparente Bereiche) in ein Punktraster um. Das ist für DTF nötig, weil DTF keine echte Halbtransparenz drucken kann — sonst entstehen steife, deckende Klumpen mit weißen Rändern. Die Punkte behalten die Originalfarben; dazwischen scheint das Shirt durch.

## Modi

- **Nur Halbtransparenz** — volle Bereiche bleiben 1:1 erhalten, nur weiche Übergänge (<100% Deckkraft) werden zu Punkten.
- **Ganzes Motiv** — komplettes Bild gerastert (Fotos/Poster), Shirtfarbe wird ausgeknockt.

## Steuerung

- **Shirt-Farbe** (Schwarz/Weiß/Grau/Custom) — Vorschau-Hintergrund + Knockout-Ziel
- **Raster** — Punktgröße (LPI), Winkel, Form (Round/Diamond/Line)
- **Tonwerte** — Weißpunkt (Deckung), Mitten (Gamma), Schwarzpunkt
- **Hartes Alpha** — Threshold gegen weiße Anti-Alias-Ränder
- **Export** — PNG bei einstellbarer Breite/DPI (Standard 300 DPI)

Statischer Single-File-Build (`index.html`), deployt via Vercel.

Built by [exe.network](https://exe.ist)
