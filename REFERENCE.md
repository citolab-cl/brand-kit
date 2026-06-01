# Citolab — Referencia de identidad visual ("Molecular Lens")

Documento detallado de marca. Para uso rápido, ver [SKILL.md](SKILL.md).
La fuente única de verdad son los archivos en `tokens/`. Esta tabla los documenta.

## 1. Paleta de color

### Marca / primarios
| Token CSS | Hex | Uso |
|---|---|---|
| `--citolab-primary` | `#2C4B7E` | **Azul marca.** Acento principal, titulares destacados, botones, encabezados de tabla. |
| `--citolab-primary-deep` | `#1E3A5F` | Azul profundo. Hover, fondos oscuros, segundo color del degradado oscuro. |
| `--citolab-tertiary` | `#0891B2` | Cian/teal. Acento secundario, subrayados, íconos, segundo color del degradado de marca. |
| `--citolab-teal-deep` | `#0F766E` | Teal profundo. Series de datos alternativas, estado "OK". |
| `--citolab-accent-soft` | `#6B89B8` | Azul medio. Detalles suaves, líneas decorativas. |
| `--citolab-blue-pale` | `#DBEAFE` | Azul muy claro. Fondos de realce, badges. |

### Texto
| Token | Hex | Uso |
|---|---|---|
| `--citolab-ink` | `#1A2332` | Texto principal. |
| `--citolab-ink-muted` | `#5A6A7E` | Texto secundario, leyendas, metadatos. |

### Superficies (claro → denso)
| Token | Hex | Uso |
|---|---|---|
| `--citolab-surface` | `#F8FAFB` | Fondo base de página/slide. |
| `--citolab-surface-card` | `#FFFFFF` | Tarjetas, contenedores, área de contenido. |
| `--citolab-surface-low` | `#F3F5F7` | Filas alternas, secciones suaves. |
| `--citolab-surface-high` | `#F0F3F5` | Realces sutiles, fondos de callout. |
| `--citolab-surface-higher` | `#E8ECEF` | Bordes de bloque, separadores densos. |

### Línea y estado
| Token | Hex | Uso |
|---|---|---|
| `--citolab-outline` | `#C8D0D4` | Bordes, divisores, líneas de tabla. |
| `--citolab-error` | `#DC2626` | Error, alerta crítica, valores fuera de meta. |
| `--citolab-success` | `#0F766E` | OK, positivo (reutiliza el teal de marca). |

### Degradado de marca
```
linear-gradient(135deg, #2C4B7E 0%, #0891B2 100%)
```
Token: `--citolab-gradient`. **Solo** en portadas, frases de impacto o títulos hero. Nunca detrás de párrafos largos.

## 2. Tipografía

| Rol | Fuente | Pesos | Detalle |
|---|---|---|---|
| Titulares | **Manrope** | 600 / 700 / 800 | Tracking apretado: `-0.04em` en títulos grandes, `-0.02em` en subtítulos. |
| Cuerpo | **Inter** | 400 / 500 / 600 | Tracking normal. Interlineado ~1.5. |
| Mono | **Geist Mono** | — | Código, datos tabulares alineados. |

Carga vía Google Fonts (ver `<head>` de las plantillas). Fallback: `system-ui, sans-serif`.

## 3. Forma y efectos

| Token | Valor | Uso |
|---|---|---|
| `--citolab-radius` | `12px` | Radio base de tarjetas/contenedores. |
| `--citolab-radius-sm` | `7px` | Badges, botones pequeños. |
| `--citolab-radius-lg` | `22px` | Bloques grandes, imágenes destacadas. |
| `--citolab-glow` | `0 0 30px rgba(44,75,126,.2)` | Resplandor azul en hover (web). |
| `--citolab-shadow-card` | sombra suave | Elevación de tarjetas. |

Efectos de la web: glassmorphism (`rgba(255,255,255,.92)` + `blur(24px)`) y "teal glow" en hover.

## 4. Logos (`assets/logos/`)

| Archivo | Cuándo |
|---|---|
| `Logo-Citolab-2026_azul.png` | Logo completo sobre fondos claros. |
| `Logo-Citolab-2026_blanco.png` | Logo completo sobre fondos oscuros/azules/degradado. |
| `iso_azul.png` / `iso_blanco.png` | Isotipo solo (favicon, marca de agua, espacios pequeños). |

Respeta un margen de protección ≈ la altura del isotipo. No deformes, recolorees ni apliques sombras al logo.

## 5. Do's & Don'ts

**Sí**
- Usar siempre los tokens; un cambio en `tokens/` se propaga a todo.
- Mantener mucho espacio en blanco; el estilo es limpio y clínico.
- Jerarquía clara: un solo H1 por documento/portada.

**No**
- No inventar azules nuevos ni usar el azul viejo de Materialize (`#01579B`, `#03A9F4`).
- No usar el degradado como fondo de texto largo.
- No mezclar más de dos familias tipográficas.
- No poner texto oscuro sobre el azul de marca (usar blanco).

## 6. Accesibilidad

- Texto principal `#1A2332` sobre `#F8FAFB`: contraste AAA.
- Texto blanco sobre `#2C4B7E`: contraste AA+ (cuerpo y titulares).
- Evitar texto atenuado `#5A6A7E` en tamaños < 12px sobre fondos de color.

## 7. Sincronización con la web

Estos tokens reflejan `src/app/globals.css` de la landing (proyecto `Landingpage`).
Si la web cambia su paleta, actualizar `tokens/citolab-tokens.css` y `.json` aquí para mantener una sola fuente de verdad.
