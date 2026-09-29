# MK Cotizador — generador de cotizaciones Mono Kids

Genera la cotización de mueble con el diseño del catálogo 2026: el vendedor
elige cliente, muebles, cantidad y acabado; el sistema calcula envío por zona,
instalación, personalización Nivel 2, plazo y total, y produce un PDF 16:9.

## Cómo se usa
1. Abrir `index.html` en Chrome (doble clic, o servir la carpeta con `python3 server.py`).
2. Llenar el panel izquierdo. El documento se arma en vivo a la derecha.
3. **Descargar PDF** → en el diálogo de impresión: destino *Guardar como PDF*,
   márgenes *Ninguno*, activar *Gráficos de fondo*.

## Reglas que implementa (no se editan acá — se citan)
- Precios: `4-documentos/lista-de-precios-mono-kids.md` (v2). Copiados en `catalogo.js`.
- Envío: incluido en Lima A–E desde S/. 1,200, tarifa por zona debajo, tachado visible.
- Instalación: S/. 120 hasta 2 muebles, S/. 200 de 3 a 5.
- Nivel 2: +10% color · +15% medida · +20% acabado, tope +40%, nunca con descuento.
- Descuento: máx. 5% con motivo; 5–10% pide Gerencia. El total siempre es la suma.
- Color cerrado obligatorio: no existe "por definir".
- Correlativo en localStorage (arranca en MK-2026-0141), editable.

## Diseño
- Formato 16:9 (1280×720 por página), paleta y tipografías del catálogo:
  Random Wednesday (titulares) + Poppins. Assets extraídos del catálogo final
  2026 y del Figma de Bruno. Fotos: CDN de Shopify (requiere internet).
