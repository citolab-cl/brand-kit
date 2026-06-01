---
name: citolab-brand
description: Aplica la identidad visual de Citolab (sistema "Molecular Lens") a informes PDF, presentaciones HTML/web, documentos y cualquier material. Provee tokens de color, tipografía, logos y plantillas listas. Usar cuando se cree o diseñe un informe, presentación, slide, propuesta, documento, portada o PDF para Citolab, o cuando se mencionen colores/estilos/marca de Citolab.
---

# Citolab Brand Kit — "Molecular Lens"

Identidad visual unificada de Citolab (laboratorio de histopatología). Úsala para que informes, presentaciones y documentos se vean consistentes con la web y entre sí.

## Quick start

1. **Color y tipografía** → importa `tokens/citolab-tokens.css` y usa las variables `--citolab-*`. Nunca escribas hex sueltos: usa los tokens.
2. **Informe / PDF** → copia `templates/informe.html` + `templates/citolab-print.css`, reemplaza el contenido, exporta a PDF (ver abajo).
3. **Presentación / slides** → copia `templates/presentacion.html`, edita las `<section>`.
4. **Logos** → en `assets/logos/` (azul sobre claro, blanco sobre oscuro; `iso_*` = isotipo solo).

## Lo esencial de la marca

- **Azul marca** `#2C4B7E` — color ancla, presente en web vieja y nueva. Es el acento principal.
- **Cian/teal** `#0891B2` — acento secundario.
- **Degradado de marca** `#2C4B7E → #0891B2` — solo para portadas y frases de impacto.
- **Titulares** Manrope (bold, tracking apretado). **Cuerpo** Inter.
- **Texto** `#1A2332` sobre fondo `#F8FAFB`. Tarjetas en blanco.

Tabla completa de tokens y reglas de uso: ver [REFERENCE.md](REFERENCE.md).

## Workflow: crear un informe PDF

1. Copia `templates/informe.html` y `templates/citolab-print.css` a tu carpeta de trabajo (mantén juntos los dos; el HTML enlaza al CSS y al logo).
2. Reemplaza título, metadatos y secciones. Usa las clases `.callout`, `.kpi-row`, tablas.
3. Exporta a PDF:
   - **Rápido:** abre el HTML en Chrome → Imprimir → "Guardar como PDF" → márgenes "Predeterminado", activa "Gráficos de fondo".
   - **Automatizable:** `chrome --headless --disable-gpu --print-to-pdf=informe.pdf --no-pdf-header-footer informe.html`

## Workflow: crear una presentación

1. Copia `templates/presentacion.html`.
2. Edita cada `<section>`. Clase `cover` = slide con degradado de marca; `accent` en `<h2>` = subrayado teal; `brand-gradient` = texto con degradado.
3. Ábrela en el navegador. Navega con flechas; `S` = notas, `F` = pantalla completa, `E` + imprimir = exportar a PDF.

## Reglas de oro (no romper)

- Un solo azul de marca: `#2C4B7E`. No inventes azules nuevos.
- Degradado solo en portadas/impacto, nunca en bloques de texto largo.
- Titulares Manrope, cuerpo Inter. No mezclar otras fuentes.
- Contraste: texto oscuro sobre claro; sobre azul/degradado, texto blanco.
- Logo azul sobre fondos claros, logo blanco sobre fondos oscuros.

Para fundamentos, do's & don'ts y accesibilidad: [REFERENCE.md](REFERENCE.md).
