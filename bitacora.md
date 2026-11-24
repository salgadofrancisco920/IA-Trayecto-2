# Paso a paso de la solucion y estructura del promt con el cual se desarrollo el asistente de IA y como se le implementaron cosas poco a poco.

#### WEEK 1
#### Creacion de Asistente IA y su interfaz con las funciones principales de estado.
---

### Como llegamos a este promt y los parametros que tuvimos en cuenta:

1. **Dividimos la celula y a cada integrante se le asigno una tarea para luego juntar las ideas y tener una ideageneral con las caracteristicas que quisimos implementar cada integrante**

2. **Luego hicimos una seleccion para ver que conceptos sobraran o estaban repetidos asi llegamos a la estructura final del promt puliendo pequeños detalles**

3. **Con ayuda de Gemini implementamos el conocimiento del trayecto 1 el cual era pedirle a una IA que nos hiciera un promt final para luego mandarselo a otra IA, esta nos dio el siguiente promt el cual fue ejecutado en Claude y posteriormente Claude devolvio el promt realizado en dos archivos los cuales fueron "HTML" y "CSS"**
## Promt final

<role>
Actúa como un Arquitecto Frontend Senior y Diseñador UI/UX especializado en interfaces conversacionales escalables, diseño modular y asistentes de IA. Tu tarea es evolucionar una maquetación HTML/CSS/JS autocontenida existente sin romper su identidad visual ni su base de código.
</role>

<input_baseline>
Toma como base el archivo `index.html` actual del proyecto **TYR — Inteligencia con carácter** (estética futurista minimalista nórdica, tipografías `Cinzel` y `Sora`, variables CSS `--bg-obsidian`, `--bg-slate`, `--bg-glass`, `--metal-titanium`, `--metal-silver`, `--metal-gradient`, `--accent-cyan`, `--accent-e merald`, `--status-warning`, `--status-error`, logotipo SVG circular con runa Tiwaz, burbuja flotante inferior izquierda, panel conversacional, mock de WhatsApp Web de fondo y barra de desarrollo `#devSwitcher`).
</input_baseline>

<requested_changes>
Aplica los siguientes cambios y mejoras manteniendo todo en un único archivo `index.html` limpio, escalable y listo para conectar en el futuro un agente real de inteligencia artificial:

1. **Unificación y escalabilidad de los estados (Vacío, Cargando, Respuesta, Error):**
   - Unifica la gestión de estados bajo un gestor de estado centralizado y escalable (por ejemplo, un objeto/controlador `TyrStateManager` o `appState` con historial de mensajes/eventos y estado actual `'empty' | 'loading' | 'response' | 'error'`), preparado para enchufar en el futuro un servicio/agente de IA real (ej. `async function runTyrAgent(payload)`).
   - Haz que los estados se integren de forma coherente y escalable en la vista del panel (permitiendo que el usuario vea el contexto/historial o los bloques de estado sin que queden sueltos ni desconectados al enviar mensajes, cambiar de tono o reintentar).
   - Mantén y mejora el envío de mensajes ficticios desde el compositor (`#composerInput` y `#composerSend`) y desde las sugerencias rápidas para que agreguen mensajes/turnos ficticios de forma limpia y predecible.

2. **Opción para mostrar y ocultar los estados (barra de pruebas / panel de estados):**
   - Agrega un botón/control claro y discreto para **mostrar u ocultar** la barra/selector de estados (`#devSwitcher`), de modo que se pueda colapsar cuando se quiera revisar la interfaz limpia y volver a desplegar cuando se necesite alternar estados manualmente.

3. **Transiciones desde "Cargando" hacia "Respuesta" y hacia "Error":**
   - Crea funciones claras y explícitas para que, al estar en **Cargando** (o al lanzar una petición/simulación de carga), se pueda avanzar/resolver tanto hacia **Respuesta** (ej. `resolveToResponse(...)`) como hacia **Error** (ej. `resolveToError(...)`).
   - Incluye controles accesibles para probar ambos caminos desde la carga/simulación (por ejemplo: que el flujo normal resuelva a respuesta, un botón/acción rápida para "Forzar error al cargar" o "Simular fallo en carga", y que al pulsar "Volver a intentar" en Error pase por Cargando y pueda resolverse de nuevo). Asegúrate de limpiar siempre temporizadores (`setTimeout` / `setInterval`) para evitar estados cruzados o fugas de timers.

4. **Fuente ficticia inventada pero realista en el bloque de fuentes:**
   - En el estado/bloque de respuesta, incorpora una **fuente ficticia** bien estructurada junto con la referencia al chat de WhatsApp (por ejemplo, un documento interno o bitácora ficticia como *"Bitácora Comercial Q4 — Propuestas y Presupuestos (Documento interno ficticio)"*, con enlace ficticio de ejemplo `https://docs.tyr-internal.example/propuestas-q4`, fecha de consulta ficticia y referencia/fragmento asociado), dejando claro que es una fuente ficticia de maquetación.
</requested_changes>

<technical_and_visual_rules>
- **Identidad y colorimetría:** Conserva la paleta oscura metálica + cian/esmeralda y las tipografías `Cinzel` y `Sora`.
- **Código autocontenido y limpio:** Entrega el archivo `index.html` completo, sin omisiones ni marcadores tipo `// resto del código aquí`.
- **Preparado para agente de IA:** Estructura el código JS en capas claras (Estado, Simulación/Agente ficticio, Renderizado/UI, Eventos) para que en la siguiente fase solo haya que reemplazar la capa de simulación ficticia por llamadas a un backend/agente real.
</technical_and_visual_rules>

<output_format>
1. **Resumen de cambios y arquitectura escalable:** Explica brevemente cómo quedan unificados los estados, cómo funciona el toggle para mostrar/ocultar estados, cómo se manejan las transiciones desde carga a respuesta/error y dónde enchufar el futuro agente de IA.
2. **Archivo `index.html` completo:** El código HTML + CSS + JS listo para guardar y abrir en el navegador.
</output_format>

### La enseñanza y lo que aprendimos:
#### Enseñanza:
1. **Tener una idea clara aparte de ahorrarte mucho tiempo te ayuda a evitar muchisimas cosas y ayuda a la IA de no alucinar con tanta informacion mezclada.**

2. **Gracias a tener una base solida nos ayuda a dejar el terreno preparado por si queremos hacer nuevas implementaciones, mejoras o elimnar conceptos que ya no nos convencen o simplemente ya no nos sirven**
#### Lo que aprendimos:
1. **Tener un flujo de trabajo mucho mas ordenado nos ayuda a tener mas control respecto a las actividades que estamos haciendo y nos ayuda a direccionar mejor cual es el siguiente paso que vamos a dar**
---
#### WEEK 2
#### Implementacion de Privacidad, Sesgos, Explicabilidad, Consentimiento, Divulgacion, Alto impacto
---
### Como llegamos a este promt y lo que tuvimos en cuenta:
1.
2.
## Promt final

11
11
11

### Lo que aprendimos:
---

