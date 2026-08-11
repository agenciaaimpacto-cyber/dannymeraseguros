# Proyecto Seguros — contexto inicial

Notas trasladadas desde la sesión de Radar Comercial (11 agosto 2026) para arrancar este proyecto sin perder contexto.

## Qué se quiere construir
Un sitio para el negocio de seguros de Danny (agente de seguros, primer mes: $874.000 CLP), con:
- Despachos de noticias del rubro seguros (mismo modelo que Radar Comercial: automatizado, investigación real con fuentes verificables)
- Ejemplos de devoluciones/siniestros evaluados (casos reales o representativos de cómo se resuelven reclamos)
- Otros elementos a definir en esta nueva conversación

## El problema real que esto resuelve (clave para priorizar decisiones)
Danny es agente de seguros y además corre campañas para otros agentes. Las campañas son mensajes directos a WhatsApp:
- Una parte de quienes responden no califica (restricciones propias del producto/campaña).
- Otra parte sí califica y conversa, pero **corta la conversación** justo cuando se le pide enviar documentos sensibles: resumen del crédito, póliza del seguro, foto del carnet de identidad.
- La hipótesis de Danny es que ese abandono es, en buena parte, un problema de **confianza**: mucha gente revisa el perfil/redes del agente antes de mandar esos documentos, y si no ve nada (o algo desactualizado), no sigue.

**Por eso el sitio + redes sociales no son el producto final, son la capa de confianza del embudo de WhatsApp**: cuando alguien que está conversando por WhatsApp entra a mirar el perfil, tiene que encontrar información real, movimiento visible y contenido actualizado (igual que Radar Comercial genera despachos diarios) — eso incluye el sitio de noticias/información del rubro, casos de devoluciones/siniestros resueltos, y redes sociales activas con carruseles diarios (mismo motor que Radar Comercial: generación automática de carruseles para Instagram/TikTok a partir del contenido investigado).

Esto debería guiar las decisiones de contenido y diseño: todo tiene que transmitir "esto es real, está activo, y esta persona/agencia responde y resuelve" — no es un sitio corporativo genérico.

## El negocio central: devolución de seguro de desgravamen
Los créditos vienen con un seguro de desgravamen atado por convenio entre la institución financiera (banco/casa comercial) y una aseguradora específica — no necesariamente la más conveniente ni económica para el cliente. El cliente tiene derecho a cambiarse de seguro de desgravamen, pero rara vez se le informa.

El servicio que ofrece la empresa para la que Danny trabaja como agente:
1. Rescata lo que queda de la prima no utilizada del seguro actual y reclama esa devolución.
2. Contrata un seguro de desgravamen nuevo, más barato (menor costo operativo).
3. El cliente recibe devolución + un seguro más económico.

**Dato clave para contenido:** mientras menos cuotas del crédito estén pagadas, mayor es la devolución posible, porque se ha consumido menos prima contratada. Útil para generar curiosidad en quien recién empezó a pagar.

Adicionalmente se pueden vender otros seguros (salud, vida, automotriz) como línea secundaria — el sitio también debería permitir que la gente quiera cotizar estos.

**Restricción importante:** no se puede gestionar portabilidad de seguro de desgravamen con créditos Hipotecarios, Cajas de Compensación, ni Forum. Vale la pena dejar esto explícito en el sitio (sección "¿aplica para tu crédito?") para filtrar de entrada a quienes no califican — reduce el problema original de leads que escriben pero no califican.

**Documentos que se piden y por qué (importante explicarlo en el sitio, no solo pedirlo):**
- Resumen del crédito: para ver cantidad de cuotas, cuotas pagadas a la fecha, monto total del crédito, número de operación.
- Póliza del seguro actual: número y compañía, para calcular su valor y buscar una mejor alternativa.
- Foto del carnet de identidad: para verificar que los documentos enviados corresponden a la persona.

## Nota de idioma
El proyecto es para Chile. Evitar acentos/voseo argentino (vos, tenés, etc.) al escribir contenido o conversar sobre el proyecto — usar español neutro/chileno estándar (tú), sin necesidad de modismos chilenos.

## Decisiones de estructura del sitio (confirmadas)
- **Nombre del sitio/marca:** Danny Mera Seguros (coincide con Instagram `dannymera.seguros`, para dar consistencia entre sitio y redes).
- **Estructura de secciones:**
  1. Inicio — gancho directo sobre el derecho a devolución de desgravamen.
  2. Cómo funciona la devolución de desgravamen — mecanismo explicado.
  3. Casos de devoluciones obtenidas — casos reales, nombres inventados.
  4. Qué documentos pedimos y por qué — resumen de crédito, póliza, carnet, explicados uno por uno.
  5. Otros seguros (salud, vida, automotriz) — cross-sell, CTA a cotizar.
  6. Noticias del rubro — despachos diarios (mismo motor que Radar Comercial).
  7. Sobre Danny — honesto: 28 años en ventas (no específicamente seguros). Afiliación real y verificable: Agente Comercial de **Grupo Insurex** (marca comercial **Mueve Seguro**). Negocio 100% online — **no se muestra dirección de oficina** en el sitio, solo fono/WhatsApp y email (+56 9 4013 0088 / danny.mera@grupoinsurex.cl). Ver borrador en `contenido/sobre-danny.md`.
  8. Contacto / WhatsApp — botón directo, no formulario.
- **Casos de devoluciones:** son casos reales de Danny, con nombres inventados para anonimizar y la institución generalizada a su categoría ("banco", "casa comercial", "financiera") en vez del nombre real, para no dar pistas de la fuente de los datos. No se guardan datos reales de clientes identificables en archivos de este proyecto. Formato confirmado: tarjetas individuales en el sitio + versión carrusel para redes (mismo contenido reutilizado). Ver `contenido/casos-devolucion.md`.

## Contexto relevante de hoy
- Danny ya tiene experiencia construyendo esto: **Radar Comercial** (`/Users/danny/Documents/Danny Mera/Proyecto Radar Comercial`) es un sitio de despachos diarios 100% automatizado (investigación web + redacción + publicación) que corre solo desde el 8 de agosto de 2026, sin fallas desde que se resolvió un problema de permisos de GitHub.
- Ese mismo proyecto también genera carruseles diarios para redes sociales (Instagram/TikTok) a partir del contenido investigado.
- Danny está separando intencionalmente sus negocios en carpetas distintas (una por proyecto) para no dispersar el foco — este es uno de varios negocios que está explorando (los otros: consultoría de "sistemas comerciales" con detección de fugas usando GoHighLevel, un negocio de turismo en Panguipulli, y una idea de cámaras de seguridad con IA, todavía sin desarrollar).
- El motor técnico de Radar Comercial (agente automatizado en la nube que investiga y publica solo, vía GitHub + Netlify) es reutilizable como base técnica para este proyecto de seguros, si se decide construirlo así.

## Cómo se configuró Radar Comercial (guía técnica reutilizable)

Si este proyecto se construye con el mismo esquema (sitio estático + automatización diaria en la nube), estos son los pasos que se siguieron, en orden. Se puede repetir tal cual:

**1. El sitio en sí**
- HTML/CSS estático simple (sin framework), sin build step — más fácil de mantener y de editar tanto por Danny como por un agente automatizado.

**2. Hosting: Netlify**
- Se crea un sitio en Netlify conectado al repositorio de GitHub del proyecto.
- Con "Deploys from GitHub" activado, cada `git push` a la rama `main` dispara un despliegue automático — no hace falta hacer nada manual para publicar.

**3. Repositorio: GitHub**
- El código vive en un repo de GitHub (en el caso de Radar Comercial: `agenciaaimpacto-cyber/radar-comercial`).

**4. Permiso de escritura para el agente automatizado (paso que costó resolver, ojo acá)**
- Para que una tarea programada en la nube pueda hacer `git push` sola, hace falta instalar la **GitHub App de Claude** con permiso de escritura sobre el repo — no alcanza con solo "conectar GitHub" desde el chat (eso da acceso de lectura nomás).
- Instalación: ir a `https://github.com/apps/claude/installations/new`, elegir la cuenta, seleccionar el repo (o "All repositories"), y confirmar con "Install & Authorize". Tiene que aparecer explícitamente el permiso **"Read and write access to code"** en la pantalla de instalación — si no aparece, es la conexión equivocada.
- Se puede verificar en `https://github.com/settings/installations` que la app "Claude" esté instalada (no solo autorizada como conexión OAuth, que es una cosa distinta y no alcanza).

**5. La tarea programada (rutina automática diaria)**
- Se crea desde `/schedule` o en `claude.ai/code/routines`, apuntando al repo de GitHub.
- Corre con modelo Sonnet 5, herramientas: Bash, Read, Write, Edit, Glob, Grep, WebSearch (y si hay generación de imágenes, se le agrega Bash con Python/Pillow).
- El prompt de la tarea debe incluir: (a) instrucciones específicas de qué investigar/generar cada día, (b) un chequeo de fecha para no duplicar contenido si ya corrió ese día, y (c) la instrucción explícita de hacer commit + push directo a `main` al final.

**6. Cómo probarlo antes de confiar en él (importante, no saltear este paso)**
- Antes de dejar la tarea corriendo "en piloto automático", se corrió manualmente un par de veces (botón "Ejecutar ahora" / acción `run` de la rutina) para confirmar que:
  1. El push a GitHub realmente funciona (ahí fue donde apareció el problema de permisos).
  2. El contenido generado tiene la calidad y el formato esperado.
- Para probar sin esperar al día siguiente, se le agregó temporalmente una nota al prompt tipo "esto es una prueba manual, ignorá el chequeo de fecha" — y después de confirmar que funciona, se vuelve a dejar el prompt original (con el chequeo de fecha) para el uso real diario.

**7. Piezas adicionales que se sumaron después (opcional, según lo que necesite este proyecto)**
- Generación de imágenes (carruseles) usando Python + Pillow con fuentes propias incrustadas en el repo (para no depender de fuentes del sistema en el entorno de la nube).
- Una página de descarga no listada (`noindex`, sin link en el menú) para bajar el material generado.

## Cómo seguir
Al abrir una sesión de Claude Code en esta carpeta, este archivo da el contexto — se puede pedir directamente "seguimos armando el sitio de seguros" y continuar desde acá.
