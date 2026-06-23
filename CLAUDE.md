# CLAUDE.md — Página Web Personal · Astro

## ⚠️ MODO APRENDIZAJE (lo más importante)

Emi NO sabe Astro. El objetivo de este proyecto es **que aprenda mientras construye**, no solo terminar el sitio. Esto cambia cómo trabajás:

- **Antes de cada cambio**: explicale qué vas a hacer y POR QUÉ — en lenguaje simple, sin asumir conocimiento previo de Astro.
- **Cuando aparezca un concepto nuevo de Astro** (file-based routing, islands, frontmatter, content collections, layouts, slots, etc.): pará y explicalo con palabras de todos los días, con una analogía si ayuda. No avances hasta que confirme que entendió.
- **Después del cambio**: contale qué hizo el código que escribiste, conceptualmente. Si hubo algo no-obvio (una decisión de diseño, una convención de Astro), explicá el porqué.
- **Lo gramatical importa menos que lo conceptual.** Si escribiste `<Image src={img} />` no hace falta explicar que `<>` es JSX y `{}` es expresión — sí hace falta explicar qué hace `<Image>` vs un `<img>` normal y por qué Astro lo provee.
- Si dudás entre "ir más rápido" o "explicar más", **siempre elegí explicar**. Preguntale si quiere más detalle o seguir.

## Ubicación y fuente de verdad
- Este archivo: `<ruta del proyecto nuevo>/CLAUDE.md` (Claude Code lo lee al inicio de cada sesión).
- Fuente de verdad de diseño y propósito: `Proyecto_Pagina_Web_Personal.md` (mismo directorio o Google Drive). Ante dudas de QUÉ va o POR QUÉ, manda ese doc.
- Metodología técnica reutilizable: `Metodologia_Claude_Code_Astro.md` (no específica de este proyecto, aplica a cualquier proyecto Astro).

## Qué es esto
Página web personal de Emiliano Caroprese, construida con Astro. Propósito y alcance del MVP: <pendiente — definir con Claude chat>.

Stack:
- **Framework:** Astro <versión>
- **Lenguaje:** TypeScript
- **Estilos:** <Tailwind / vanilla CSS / UnoCSS — pendiente>
- **Content:** <Markdown / MDX / Content Collections — pendiente>
- **Deploy:** <Cloudflare Pages / Vercel / Netlify / GitHub Pages — pendiente>
- **Dominio:** <pendiente>
- **Repo:** <pendiente>

## Estructura del repo
- `src/pages/` — file-based routing (cada `.astro` es una URL)
- `src/components/` — componentes reutilizables
- `src/layouts/` — layouts compartidos entre páginas
- `src/content/` — content collections (si se usan)
- `src/assets/` — imágenes optimizadas vía `<Image>`
- `public/` — assets estáticos servidos tal cual
- `astro.config.mjs` — config del framework
- `tsconfig.json` — config TypeScript

## Secciones de la página (definir con Claude chat)
- <ej: Home / Sobre mí>
- <ej: Proyectos / Portfolio>
- <ej: Blog>
- <ej: Contacto>

## Método de trabajo (resumido — el detalle vive en Metodologia_Claude_Code_Astro.md)
1. Antes de tocar nada: `git status` + arrancar `npm run dev` para verificar baseline.
2. Planificar: qué archivos se tocan, qué impacto en componentes vecinos / layouts compartidos.
3. Cambio mínimo. Verificar visualmente en `localhost`.
4. `npm run build` antes de commitear para confirmar que no rompió producción.
- Un cambio a la vez. Si algo rompe, `git diff` antes de proponer fix.
- Para cambios UI, screenshot o testeo en browser **antes** de decir "listo".

## Errores conocidos y fixes
(Vacío al arranque. Se llena con la experiencia de este proyecto. Los gotchas reutilizables de Astro en general viven en `Metodologia_Claude_Code_Astro.md` sección 8.)

## Estado actual
- Pendiente: scaffolding inicial (`npm create astro@latest`).
- Pendiente: decisiones de stack (estilos, deploy) y secciones del MVP.
- Pendiente: primer commit.
