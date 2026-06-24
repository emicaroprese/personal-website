# CLAUDE.md — Página Web Personal · Astro

## ⚠️ MODO APRENDIZAJE (lo más importante)

Emi NO sabe Astro. El objetivo de este proyecto es **que aprenda mientras construye**, no solo terminar el sitio. Esto cambia cómo trabajás:

- **Antes de cada cambio**: explicale qué vas a hacer y POR QUÉ — en lenguaje simple, sin asumir conocimiento previo de Astro.
- **Cuando aparezca un concepto nuevo de Astro** (file-based routing, islands, frontmatter, content collections, layouts, slots, etc.): pará y explicalo con palabras de todos los días, con una analogía si ayuda. No avances hasta que confirme que entendió.
- **Después del cambio**: contale qué hizo el código que escribiste, conceptualmente. Si hubo algo no-obvio (una decisión de diseño, una convención de Astro), explicá el porqué.
- Si dudás entre "ir más rápido" o "explicar más", **siempre elegí explicar**.

## Fuentes de verdad
- Diseño y propósito: `Proyecto_Pagina_Web_Personal.md` (mismo directorio).
- Metodología técnica reutilizable: `Metodologia_Claude_Code_web.md` (mismo directorio).

## Qué es esto
Landing de servicios + portfolio personal de Emiliano Caroprese. Single-page con scroll, orientada a clientes potenciales.

Stack:
- **Framework:** Astro 7
- **Lenguaje:** TypeScript
- **Estilos:** Tailwind CSS v4 (vía `@tailwindcss/vite`)
- **Deploy:** Vercel — `personal-website-sand-nine-38.vercel.app`
- **Repo:** https://github.com/emicaroprese/personal-website

## Estructura del repo
- `src/pages/index.astro` — página principal (única). Contiene las 4 secciones.
- `src/layouts/Layout.astro` — navbar + HTML base compartido
- `src/styles/global.css` — activa Tailwind (no tocar)
- `public/` — assets estáticos (favicon)
- `astro.config.mjs` — config del framework

## Secciones de la página
Single-page con scroll. Todas viven en `src/pages/index.astro`:
1. **Home** (`#home`) — nombre, bajada, CTA de contacto
2. **Proyectos** (`#servicios`) — 3 proyectos con placeholder
3. **Sobre mí** (`#sobre-mi`) — párrafo corto, pendiente contenido real
4. **Contacto** (`#contacto`) — email y teléfono, pendiente datos reales

## Método de trabajo
1. Antes de tocar nada: `git status` + `npm run dev` para verificar baseline.
2. Planificar qué archivos se tocan y el impacto en el Layout si corresponde.
3. Cambio mínimo. Verificar en `localhost:4321`.
4. `npm run build` antes de commitear.
5. Commit + push → Vercel deploya automáticamente.

## Errores conocidos y fixes
- **`npm create astro@latest .`** en carpeta no vacía crea subcarpeta con nombre random en lugar de usar la carpeta actual. Fix: mover archivos manualmente a la carpeta raíz después del scaffold.
- **Caché npm con permisos root**: correr `sudo chown -R 501:20 ~/.npm` en Terminal (no funciona con `!` desde Claude Code porque necesita contraseña interactiva).

## Estado actual
Infraestructura completa. Página en vivo con las 4 secciones, diseño minimalista base, numeración 01–04, navbar con scroll suave. Contenido placeholder.
Próximo paso: diseño del hero (referencia: Dribbble shot tipografía grande + efecto fantasma en segunda línea, adaptado a modo claro).
