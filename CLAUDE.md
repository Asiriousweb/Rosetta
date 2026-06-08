# Rosetta Producciones — Sitio Web

## Qué hace la empresa

**Rosetta Producciones SpA** es una empresa chilena con más de 15 años de experiencia en **infraestructura para eventos, festivales, minería y corporativos** en Chile y Latam. Todo el equipo es 100% propio, sin intermediarios.

### Servicios principales
1. **Estructuras de escenario** — andamios modulares certificados, escenarios principales, tarimas, pórticos, torres de audio/luces, graderías, ascensores de carga, zonas VIP, pasarelas
2. **Carpas industriales** — hasta 5.000 m², resistentes al viento, climatización, piso técnico, para eventos, ferias y faenas
3. **Generación eléctrica** — generadores 30–1.000 kVA, tableros de transferencia automática, distribución certificada SEC, torres de iluminación, pasacables
4. **Logística y transporte** — flota propia de +10 camiones, cobertura norte–sur de Chile, cargas especiales, seguro incluido, coordinación 24/7

### Industrias que atiende
- **Eventos masivos**: festivales (Lollapalooza, Afterlife, Coke Studio), conciertos (Paul Anka, Rafael Nadal), Van Gogh Alive
- **Minería e industria**: Expomin, faenas remotas, campamentos, andamios Sernageomin
- **Corporativo**: Nissan Pavilion, Valle Nevado, activaciones de marca
- **Deportivo**: Juegos Panamericanos 2023, Copa Davis, Estadio Nacional

### Keywords SEO prioritarias
`estructuras para eventos Chile`, `carpas industriales arriendo`, `generadores para festivales`, `escenarios para conciertos Santiago`, `infraestructura eventos Latam`, `andamios certificados Chile`, `producción técnica festivales`

---

## Stack técnico

- **HTML + CSS + JS vanilla** — sin frameworks, sin bundler, sin dependencias npm
- **Fuentes**: Bebas Neue (display), DM Sans (body), DM Mono (mono) vía Google Fonts
- **Deploy**: Vercel (static site) → `https://rosetta-ten.vercel.app/`
- **Repositorio**: GitHub (`Asiriousweb/Rosetta`) — push via GitHub Desktop
- **Dominio pendiente**: conectar `rosettaproducciones.cl` a Vercel cuando esté disponible

---

## Archivo principal

`index.html` — todo el sitio vive en este archivo (HTML + CSS inline + JS inline)

---

## Estructura de secciones

| # | Sección | Descripción |
|---|---------|-------------|
| 1 | **Nav** | Fijo, logo imagen PNG negro, mega-dropdowns (Servicios, Industrias, Proyectos) + drawer mobile con hamburger |
| 2 | **Hero** | Fullscreen, pills de industria, headline animado, stats (15+ años, 24/7, 100% propio, Norte–Sur / Chile y Latam) |
| 3 | **Trust bar** | 4 métricas: 15+ Años · 24/7 Servicio · 100% Equipo propio · Norte–Sur / Chile y Latam |
| 4 | **Video corporativo** | Video `Video corporativo rosetta.mp4`, aspect-ratio 16/9, botón mute/unmute en esquina |
| 5 | **Industrias** | Tabs: Eventos / Minería / Corporativo / Deportivo, cada uno con cards de servicios específicos |
| 6 | **Servicios** | Grid 4 cards: Estructuras · Carpas · Energía · Logística |
| 7 | **Portafolio** | Grid 12 columnas, `grid-auto-rows: 260px`, 20+ proyectos con fotos y videos reales |
| 8 | **Diferenciadores** | Banda naranja con 4 propuestas de valor |
| 9 | **Contacto** | Canales (WhatsApp, email, Instagram) + formulario Formspree |
| 10 | **Footer** | Logo imagen blanca (filter: invert), links, copyright |
| 11 | **WA float** | Botón flotante WhatsApp esquina inferior derecha |

---

## Portafolio — proyectos actuales

Sistema de clases CSS: `.pf-card.cX` (columnas) + `.pf-card.r2` (doble fila)

| Clase | Columnas |
|-------|----------|
| `c12` | 12 (ancho completo) |
| `c7`  | 7 |
| `c6`  | 6 |
| `c5`  | 5 |
| `c4`  | 4 |
| `c3`  | 3 |

Fondos de foto usan `.pf-bg.{nombre}.bg-loaded` (lazy load via IntersectionObserver).
Videos usan `<video class="lazy-video" preload="none">` — se activan con IntersectionObserver.

**Proyectos en el grid (orden de filas):**
1. Lollapalooza 2024 — video timelapse escenario (c12, r2, hero)
2. Timelapse carpa Lolla — video (c7, r2) / Paul Anka (c5) / Nissan video (c5)
3. Panamericanos video / Copa Davis
4. Coke Studio / Generadores / Valle Nevado
5. Vendimia Valle del Maipo / Estadio Nacional / Dunalastair
6. Lollapalooza Kids / Expomin Energía video
7. Afterlife Chile — video (c12)
8. Van Gogh Alive video / Camiones Rosetta
9. Cierre Perimetral Panamericanos video / Lift Escénico video / Rampas Panamericanos
10. Rafael Nadal — video (c12, fila final destacada)

---

## Assets

```
Assets fotos/          — JPGs del portafolio
Assets Videos/         — MP4s del portafolio y corporativo
Assets Logo/           — Logo PNG negro + favicon JPEG
sitemap.xml            — Para Google Search Console
robots.txt             — Permite indexación completa
```

**Logo nav**: `Assets Logo/Logo Rosetta Producciones negro.png` (height: 38px desktop, 30px mobile)
**Logo footer**: misma imagen con `filter: invert(1) brightness(2)` para fondo oscuro
**Favicon**: `Assets Logo/LOGO FAVICON ROSSETA FONDO BLANCO LETRAS NEGRAS.jpeg`

---

## Datos de contacto (producción)

| Canal | Valor |
|-------|-------|
| WhatsApp | `+56 9 6678 9753` → `56966789753` |
| Email | `contacto@rosettaproducciones.com` |
| Instagram | `@rosettaproducciones_` |
| Fundación | Desde 2008 |

---

## Formulario de contacto

Conectado a **Formspree** (`action="https://formspree.io/f/contacto@rosettaproducciones.com"`).
Campos en orden (los `name` determinan el orden en el email recibido):
1. `01 - Nombre` (required)
2. `02 - Empresa`
3. `_replyto` (email, required)
4. `03 - Tipo de evento` (dropdown)
5. `04 - Industria` (dropdown)
6. `05 - Asistentes` (dropdown)
7. `06 - Ciudad` (texto)
8. `07 - Fecha estimada` (date)
9. `08 - Detalle del proyecto` (textarea)
10. `_subject` hidden: "Nueva solicitud de cotización — Rosetta Producciones"

**Pendiente**: verificar email en Formspree la primera vez que llegue un formulario.

---

## SEO y visibilidad

### Implementado
- Meta title, description, keywords, robots, canonical
- Open Graph completo (LinkedIn, WhatsApp, Facebook)
- Twitter/X card
- Schema.org `LocalBusiness` con servicios detallados
- `sitemap.xml` + `robots.txt`

### Pendiente (manual)
- Registrar en **Google Search Console** y enviar sitemap
- Verificar preview en **LinkedIn Post Inspector**
- Conectar dominio `rosettaproducciones.cl` a Vercel
- Actualizar `canonical` y URLs del Schema.org al dominio final

---

## Notas de desarrollo

- `scrollTo2(id)` — helper de smooth scroll; llama `closeAllNav()` antes de navegar
- `closeAllNav()` — cierra cualquier mega-dropdown abierto
- `toggleNav(id)` — abre/cierra mega-dropdown; se posiciona con `getBoundingClientRect()`
- Mega-dropdowns son `position: fixed`, DOM dentro de `.nav-item`
- Scroll reveal: `IntersectionObserver` con clase `.reveal` → `.visible`
- Lazy video: `IntersectionObserver` sobre `.lazy-video` → `.play()` / `.pause()`
- Lazy bg: `IntersectionObserver` sobre `.pf-bg.{cls}` → agrega `.bg-loaded` que activa `background-image`
- Video corporativo: `id="corp-video"`, botón `id="corp-mute-btn"`, función `toggleCorpMute()`
- `.service-card-icon:empty { display: none }` — evita desalineación por divs de icono vacíos

## Paleta de colores

| Variable | Valor |
|----------|-------|
| `--black` | `#0d0d0d` |
| `--white` | `#FAFAF8` |
| `--orange` | `#E05A1C` |
| `--orange-dim` | `#B8451A` |
| `--gray-1..6` | Escala cálida `#F2EDE6` → `#4a3f38` |

## Responsive

| Breakpoint | Grid portafolio | Notas |
|------------|----------------|-------|
| > 1024px | 12 col, 260px rows | Full layout |
| ≤ 1024px | 6 col, 220px rows | Tablets |
| ≤ 768px | 2 col, 180px rows | Mobile — nav hamburger |
| ≤ 420px | 1 col, 220px rows | Small phones |
