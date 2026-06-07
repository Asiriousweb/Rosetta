# Rosetta Producciones — Sitio Web

Landing page estática de una sola página para Rosetta Producciones SpA, empresa chilena de infraestructura para eventos (estructuras, carpas, energía, logística).

## Stack

- HTML + CSS + JS vanilla — sin frameworks, sin bundler, sin dependencias npm
- Fuentes: Bebas Neue (display), DM Sans (body), DM Mono (mono) vía Google Fonts
- Deploy: Vercel (static site), repositorio en GitHub

## Archivo principal

`index.html` — todo el sitio vive en este archivo (HTML + CSS inline + JS inline)

## Secciones

1. **Nav** — menú fijo con mega-dropdowns (Servicios, Industrias, Proyectos) + drawer mobile
2. **Hero** — fullscreen con pills de industria, headline animado y stats
3. **Trust bar** — 4 métricas clave (15+ años, 24/7, 100% propio, Norte–Sur)
4. **Industrias** — tabs con 4 paneles: Eventos, Minería, Corporativo, Deportivo
5. **Servicios** — grid de 4 cards: Estructuras, Carpas, Energía, Logística
6. **Portafolio** — masonry grid con proyectos destacados (Lolla, Afterlife, Panamericanos…)
7. **Diferenciadores** — banda naranja con 4 propuestas de valor
8. **Contacto** — canales (WhatsApp, email, Instagram) + formulario de cotización
9. **Footer** — logo, links, copyright
10. **WA float** — botón flotante de WhatsApp

## Paleta de colores

| Variable       | Valor     |
|----------------|-----------|
| `--black`      | `#0d0d0d` |
| `--white`      | `#FAFAF8` |
| `--orange`     | `#E05A1C` |
| `--orange-dim` | `#B8451A` |
| `--gray-1..6`  | Escala cálida desde `#F2EDE6` hasta `#4a3f38` |

## Datos que actualizar antes de lanzar

- Número de WhatsApp: actualmente `+56 9 1234 5678` (placeholder)
- Email: actualmente `contacto@rosettaproducciones.com` (verificar)
- Instagram: `@rosettaproducciones_` (verificar handle)
- Fotos reales para el portafolio (actualmente placeholders con gradientes + emoji)
- Año fundación en footer: "Desde 2008" (verificar)

## Notas de desarrollo

- El formulario de contacto no tiene backend — conectar a Formspree, Netlify Forms o similar al lanzar
- `scrollTo2()` es el helper de smooth scroll (evita colisión con el nativo `scrollTo`)
- Los dropdowns del nav se posicionan con JS calculando `getBoundingClientRect()`
- Scroll reveal usa `IntersectionObserver` con clase `.reveal` → `.visible`
