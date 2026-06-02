# Citolab Brand Kit — "Molecular Lens"

Identidad visual unificada de Citolab + skill de Claude Code para aplicarla a
**informes/PDF** y **presentaciones HTML**. Una sola fuente de verdad para que
web, documentos y presentaciones se vean iguales.

## Qué hay aquí

```
Branding/
├── SKILL.md                  # Skill de Claude Code (instrucciones de uso)
├── REFERENCE.md              # Guía de marca detallada (colores, tipografía, do's & don'ts)
├── tokens/
│   ├── citolab-tokens.css    # Variables CSS --citolab-*  (úsalo en cualquier HTML/CSS)
│   └── citolab-tokens.json   # Mismos tokens en JSON (para herramientas/scripts)
├── templates/
│   ├── informe.html          # Plantilla de informe → exportar a PDF
│   ├── citolab-print.css     # Estilos de impresión del informe
│   └── presentacion.html     # Plantilla de slides (reveal.js + tema Citolab)
└── assets/logos/             # Logos oficiales (azul / blanco / isotipo)
```

## Uso A — como skill de Claude Code (recomendado para el equipo)

Cada miembro instala el kit como skill clonándolo en su carpeta de skills:

```bash
git clone https://github.com/citolab-cl/brand-kit.git ~/.claude/skills/citolab-brand
```

Luego, en cualquier sesión de Claude Code, basta pedir *"hazme un informe / una
presentación para Citolab"* y el skill `citolab-brand` se activa solo, aplicando
colores, tipografía y plantillas correctas.

Para actualizar a la última versión de la marca:

```bash
cd ~/.claude/skills/citolab-brand && git pull
```

> Alternativa sin duplicar: clónalo donde prefieras y crea un symlink
> `ln -s /ruta/al/repo ~/.claude/skills/citolab-brand`.

## Uso B — manual (sin Claude Code)

1. **Informe PDF:** abre `templates/informe.html`, edita el contenido, e
   imprime a PDF desde el navegador (activa "Gráficos de fondo").
2. **Presentación:** abre `templates/presentacion.html`, edita las `<section>`,
   navega con las flechas. `F` = pantalla completa.
3. **Colores/tipografía en tus propios archivos:** importa
   `tokens/citolab-tokens.css` y usa las variables `--citolab-*`.

## Regla de oro

No copies códigos de color a mano: **usa siempre los tokens**. Si la marca
cambia, se edita `tokens/` una vez y todo el material queda actualizado.

Detalle completo en [SKILL.md](SKILL.md) y [REFERENCE.md](REFERENCE.md).
