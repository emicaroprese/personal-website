# Página Web Personal · Astro

_Documento de diseño y estado del proyecto_

*Fuente de verdad de propósito, diseño y decisiones. El CLAUDE.md tiene el QUÉ técnico estable; este doc tiene el POR QUÉ. El as-built técnico vive en el código del repo.*

# 0. Objetivo principal del proyecto: APRENDIZAJE

**Emi no sabe Astro.** El sitio web es el resultado, pero el verdadero objetivo es **aprender Astro construyendo este sitio**. Esto cambia las reglas del juego:

- **El ritmo lo marca el aprendizaje, no la velocidad de entrega.** Tener todo el MVP en 2 días sin entender nada es FRACASO. Tener la mitad en 2 semanas y entender cómo funciona es ÉXITO.
- **Toda decisión técnica se explica.** Tanto Claude chat (para decisiones de diseño/arquitectura) como Claude Code (para implementación) tienen que explicar el por qué de cada cosa en lenguaje simple.
- **No importa la perfección gramatical o de estilo del código** — importa entender qué hace cada pieza y por qué está ahí.
- Si en algún momento Claude (chat o code) avanza sin que Emi entienda, **se detiene y se explica**. No es opcional.

Este principio prima sobre cualquier otra prioridad del proyecto.

# 1. Visión general

Landing de servicios + portfolio personal de Emiliano Caroprese. Una sola página con scroll, orientada a clientes potenciales y conocidos que quieran ver los proyectos y servicios que ofrece Emi.

| Dato | Valor |
| --- | --- |
| Fase actual | Definición cerrada — listo para scaffolding |
| Stack | Astro + Tailwind CSS |
| Deploy | Vercel |
| Dominio | Pendiente (por ahora `.vercel.app`) |
| Repo | Pendiente de crear |

# 2. Propósito y audiencia

**¿Quién entra y por qué?**
Visitante principal: clientes potenciales (gente que podría contratar los servicios de Emi) y conocidos / contactos. Entran para ver los proyectos ya realizados y los servicios que ofrece. La página funciona como **landing de servicios + portfolio**, no como CV para reclutadores ni como blog.

**¿Qué querés que haga el visitante? (CTA)**
Acción principal: **que se contacte con Emi**. Medios de contacto: teléfono (vía QR + link directo) y email.
Acción secundaria: ver los proyectos en detalle.
> Nota: el QR sirve para contextos donde la web se ve en otra pantalla (tarjeta física, web en compu). Para quien entra desde el celu hace falta también un link de contacto directo. A afinar en diseño.

**¿Qué impresión dejar?**
**Minimalista** — limpio, mucho espacio en blanco, poco texto, elegante por sustracción.

**Nota general:** el sitio es un **mock** de aprendizaje. Los 3 proyectos pueden llevar contenido placeholder; no se requieren proyectos finalizados ni datos reales todavía.

# 3. Contenido y secciones

**Estructura:** una sola página con scroll (single-page) + menú de navegación arriba que salta a cada sección.

**Home (inicio)**
- Va: nombre de Emi + 2-3 líneas de quién es / qué hace + botón principal de contacto (CTA).
- Tono: directo y limpio. Lo primero que se ve.
- No va: textos largos ni párrafos de presentación (eso es Sobre mí).

**Servicios / Proyectos**
- Va: los 3 trabajos con título, descripción corta y opción de ver detalle:
  1. Creación de páginas web
  2. App BOH cocina
  3. BOH empresa constructora
- Tono: muestra de lo que Emi puede hacer.
- No va: contenido real por ahora — placeholder hasta que el sitio deje de ser mock.

**Sobre mí**
- Va: un párrafo corto que genere confianza en un cliente potencial.
- Tono: cercano pero profesional.
- No va: historia de vida larga.

**Contacto**
- Va: QR + teléfono + email, bien visibles. Cierre de la página.
- Tono: claro, fácil de actuar.
- No va: formulario complejo (al menos en el mock).

# 4. Estilo visual

**Referencias visuales:** mitchkoko.app · ritualz.app · mitchkoko.app/flutter

**Paleta:** fondo claro (blanco o casi blanco, tipo `#f5f5f5` o `#fafafa`), texto negro. Sin color de acento llamativo — si existe, es muy sutil.

**Tipografía:** sans-serif (letras limpias, sin remates, modernas).

**Densidad:** aireada. Mucho espacio en blanco. El espacio es parte del diseño.

**Elementos visuales:** numeración como recurso estético (01, 02, 03). Sin imágenes de fondo, sin animaciones, sin decoración extra.

**Modo oscuro:** no. Solo modo claro. Queda para v2 si se decide.

# 5. Performance / SEO / accesibilidad

- **Lighthouse:** no es prioridad para el mock. Astro da buenas notas por defecto.
- **Meta tags:** configurar título y descripción básica. Open Graph para preview al compartir link.
- **Sitemap / Robots.txt:** incluir con el plugin `@astrojs/sitemap`. Es automático.
- **Alt text:** sí en todas las imágenes, aunque sean placeholders.
- **Contraste:** el fondo claro + texto negro garantiza contraste AAA sin esfuerzo extra.

# 6. Decisiones y su fundamento

| Decisión | Elegido | Por qué |
| --- | --- | --- |
| Framework | Astro | HTML estático por defecto, performance alta, ideal para sitios de contenido |
| Estilos | Tailwind CSS | Sistema de diseño aplicable en varios frameworks; pragmático para quien no se especializa en web |
| Deploy | Vercel | Integración directa con GitHub, gratis, referencia más común en docs y tutoriales de Astro |
| Estructura | Single-page con scroll | Un solo archivo principal; ideal para aprender y para mock |
| Modo oscuro | No | Duplica el trabajo de diseño; queda para v2 |

# 7. Roadmap

**MVP (lo mínimo para publicar):**
- Página única con las 4 secciones: Home, Servicios/Proyectos, Sobre mí, Contacto
- Menú de navegación arriba con salto a cada sección
- Los 3 proyectos con contenido placeholder
- Datos de contacto (teléfono + email) y QR
- Deploy en Vercel con URL pública

**V2 (después de aprender el MVP):**
- Reemplazar placeholders por contenido real
- Página de detalle individual por proyecto
- Dominio propio (en lugar de `.vercel.app`)
- Open Graph completo para preview de links

**Largo plazo:**
- Modo oscuro
- Formulario de contacto funcional
- Blog o sección de artículos

# 8. Estado / dónde vamos

*Única sección volátil. Se actualiza al cierre de cada sesión que cambió algo.*

### Estado actual

Definición del proyecto completada. Secciones 1–7 cerradas. Listo para pasar a Claude Code y arrancar el scaffolding de Astro.

### Próximo paso

1. Crear el repo en GitHub.
2. Ejecutar `npm create astro@latest` y configurar el proyecto base.
3. Configurar Tailwind CSS en Astro.
4. Primer deploy en Vercel.

### Pendientes / decisiones abiertas

- Definir nombre del repo.
- Afinar el mecanismo de contacto (QR vs link directo vs ambos) cuando se llegue a esa sección.
- Contenido real de "Sobre mí" (para cuando deje de ser mock).

### Changelog reciente

- **Sesión 1 (inicio del proyecto):** definición completa de secciones 1–7. Stack elegido: Astro + Tailwind CSS + Vercel. Estructura: single-page. Estilo: minimalista, referencias mitchkoko/ritualz. Mock de aprendizaje confirmado.
