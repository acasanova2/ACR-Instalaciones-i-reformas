# INSTRUCCIONES GENERALES OBLIGATORIAS — Proyecto web ACR Instalaciones y Reformas

Estas instrucciones son de cumplimiento estricto para TODO el proyecto. Aplican a cada página, componente o sección que generes, edites o amplíes, no solo a la primera entrega. Si en algún momento dudas entre una opción "más bonita" y una que respeta esta guía, respeta siempre la guía.

## 1. Contexto del proyecto
Sitio web para **ACR Instalaciones y Reformas Barcelona**, empresa especializada en reformas integrales, cocinas y baños, instalaciones técnicas (electricidad, fontanería, gas, climatización) y albañilería/pintura en Barcelona y área metropolitana (Nou Barris). Público objetivo: propietarios, arquitectos y particulares que buscan una reforma de confianza, con estética cuidada, cercana y profesional (no "industrial" ni agresiva).

Tienes como referencia:
- `code.html`: la base de código real ya construida (estructura, clases Tailwind, secciones).
- `DESIGN.md`: el sistema de diseño completo (colores, tipografía, espaciados, sombras, formas, componentes).
- `screen.png`: captura de referencia visual del resultado esperado.

## 2. Reglas que NUNCA deben romperse

### 2.1 Sistema de diseño (Design Tokens)
- Usa **exclusivamente** los colores definidos en `DESIGN.md` / la configuración de Tailwind del `code.html` (paleta "Pistachio Architectural Sanctuary": verdes pistacho, salvia, plaster cálido, charcoal botánico). Prohibido introducir colores fuera de esta paleta (nada de negro puro, azules corporativos genéricos, naranjas/ámbar industriales, etc.).
- Respeta los nombres semánticos de color (`primary`, `on-primary`, `surface`, `surface-container`, `tertiary-container`, etc.) tal como están mapeados en la configuración de Tailwind del HTML. No inventes nuevos tokens de color sin necesidad.
- Tipografía: **Epilogue** para titulares/display, **Manrope** para cuerpo y micro-copy (en el código actual aparecen como Montserrat/Inter dentro de la config de Tailwind — mantener la jerarquía y los tamaños definidos, pero si hay conflicto entre `DESIGN.md` y el HTML, usar Epilogue/Manrope como fuentes oficiales, ya que son las especificadas en el DESIGN.md).
- Radios de borde: 4px (`DEFAULT`) para inputs/botones, 8px (`lg`) para tarjetas/paneles, 12px (`xl`) para módulos flotantes/imágenes, `full` solo para chips y badges tipo píldora. No uses esquinas totalmente rectas ni border-radius aleatorios.
- Sombras: solo las sombras suaves y cálidas definidas (tonos `rgba(36,43,33,...)`), nunca sombras negras duras ni contornos gruesos oscuros.
- Espaciados: respeta la escala (`space-xs/sm/md/lg/xl`, `gutter`, `margin`) y el grid de 12 columnas en desktop / 8 en tablet / 4 en mobile, con los márgenes y gutters especificados.

### 2.2 Identidad de marca y tono
- La estética es de **minimalismo arquitectónico orgánico**: cálida, natural, serena. Nada de alto contraste blanco/negro, nada de colores de "obra" tipo amarillo de seguridad o naranja industrial.
- El tono de los textos es profesional pero cercano, orientado a generar confianza (no venta agresiva ni lenguaje excesivamente técnico sin contexto).
- Mantén coherencia visual entre todas las secciones nuevas y las ya existentes en `code.html`: mismos componentes de tarjeta, mismos botones primarios/secundarios/ghost, mismos badges.

### 2.3 Estructura y contenido reales
- No inventes datos de contacto, teléfonos, direcciones o cifras (años de experiencia, número de proyectos, reseñas) distintos a los ya presentes en `code.html`/`screen.png` (ej. 670 082 313, Carrer de Joaquim Valls 39, Nou Barris 08016 Barcelona) salvo que se te pida explícitamente crear contenido nuevo, y en ese caso avisar de que son datos de ejemplo.
- Mantén las secciones y su orden lógico salvo que se indique lo contrario: Header/nav → Hero → Métricas de confianza → Servicios → Galerías de proyectos (con antes/después cuando aplique) → Testimonios/reseñas → Formulario de presupuesto → Footer.
- El CTA principal siempre debe ser "Pedir presupuesto" / contacto por WhatsApp o teléfono, visible en el header, hero y footer.

### 2.4 Código y buenas prácticas técnicas
- Usa Tailwind CSS igual que en `code.html` (misma convención de clases utilitarias), reutilizando la configuración de tema (`tailwind.config`) ya definida; no dupliques ni redefinas tokens que ya existen.
- HTML semántico (`header`, `main`, `section`, `footer`, etiquetas de encabezado jerárquicas `h1`-`h3`).
- Diseño **responsive obligatorio**: mobile, tablet y desktop, siguiendo los breakpoints y comportamientos descritos en `DESIGN.md` (columnas que colapsan, touch targets mínimos de 44px).
- Accesibilidad básica: contraste adecuado usando los pares `on-*` de la paleta, atributos `alt` en imágenes, `label` asociados a inputs del formulario.
- No añadir dependencias, frameworks o librerías externas que no estén ya presentes en `code.html` (Tailwind vía CDN) salvo que lo pida explícitamente.
- Todo el contenido y las etiquetas visibles deben estar en **español**.

## 3. Qué hacer ante ambigüedad
Si una petición no especifica un detalle (color exacto, tamaño, copy), resuélvelo siguiendo el sistema de diseño de `DESIGN.md` y el estilo ya visible en `code.html`/`screen.png`, en vez de usar valores por defecto genéricos de Tailwind o de otro framework.

## 4. Entregable
Cada vez que generes o modifiques código, el resultado debe ser HTML válido, coherente con `code.html`, y visualmente alineado con `screen.png`. No reescribas secciones enteras que ya funcionan bien salvo que se solicite explícitamente.
