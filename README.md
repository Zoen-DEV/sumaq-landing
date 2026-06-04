# Sumaq Studios — Web Corporativa

Página web de [Sumaq Studios](https://sumaqstudios.com), estudio de diseño y desarrollo digital. Construida con Astro 5, Tailwind CSS 4 y GSAP para animaciones avanzadas.

## Stack

| Herramienta | Versión | Rol |
|---|---|---|
| [Astro](https://astro.build) | 5.0 | Framework / generador de sitio |
| [Tailwind CSS](https://tailwindcss.com) | 4.0 | Estilos utilitarios |
| [GSAP](https://gsap.com) | 3.15 | Animaciones y ScrollTrigger |
| TypeScript | 5.7 | Tipado estático |

## Inicio rápido

```bash
# Instalar dependencias (primera vez: aprobar builds nativos)
pnpm approve-builds esbuild sharp
pnpm install

# Servidor de desarrollo (http://localhost:4321)
pnpm dev

# Validar TypeScript
pnpm check

# Build de producción
pnpm build

# Previsualizar build local
pnpm preview
```

## Estructura

```
src/
├── layouts/
│   └── BaseLayout.astro      # HTML base, meta tags, tema claro/oscuro
├── components/
│   ├── Nav.astro             # Navegación sticky + theme toggle
│   └── Footer.astro
├── pages/
│   ├── index.astro           # Homepage: hero, servicios, proceso, manifiesto, FAQ, contacto
│   ├── servicios.astro       # Detalle de servicios
│   ├── proceso.astro         # Proceso de trabajo
│   └── faq.astro             # Preguntas frecuentes
└── styles/
    ├── tokens.css            # Sistema de diseño: colores, tipografía, espaciado, easing
    └── global.css            # Reset y estilos base

public/
├── fonts/                    # Geist Variable (auto-hosted)
├── logo/                     # Wordmarks SVG (modo claro e invertido)
└── favicon.svg
```

## Características

- **Multi-página** con navegación compartida (Nav + Footer como componentes Astro)
- **Sección de contacto exclusiva en homepage** — el CTA "Hablemos" redirige a `/#contacto` desde otras páginas
- **Animaciones scroll-driven**: parallax, reveals por palabra, spotlight en cards, manifesto pinned con scrub
- **Tema claro/oscuro**: toggle persistido en `localStorage`, respeta `prefers-color-scheme`
- **Reduced-motion**: todas las animaciones se desactivan automáticamente si el usuario lo prefiere
- **Tipografía local**: Geist Variable sin dependencias externas
- **CTA magnéticos**: botones con hover elástico via `gsap.quickTo`

## Despliegue

El sitio está configurado para `https://sumaqstudios.com`. Genera HTML estático en `dist/` — compatible con cualquier CDN o hosting estático (Vercel, Netlify, Cloudflare Pages).

## Contacto

enzoholgadodev@gmail.com
