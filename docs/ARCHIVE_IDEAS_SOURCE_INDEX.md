# Inventario inicial de ideas — archivo Proyecto-Matter.zip

**Fecha de revisión:** 2026-11-19. **Estado:** clasificación inicial, no auditoría íntegra de cada apartado de las ~16 970 líneas del archivo. Se preserva la prioridad del trabajo ya iniciado en Base-Matter y la prohibición de iniciar Bot-Matter antes de completar criterios.

## Regla de incorporación al ecosistema

Cada idea se convierte primero en una **necesidad verificable**, no en código ejecutable por haber sido mencionada. El responsable debe crear especificación, autorización/política, límites, plan de pruebas, riesgos, dependencias y criterio de aceptación. Estado permitido: `idea → investigación → requisitos aprobados → prototipo → probado → desplegado`.

**Privacidad:** el archivo contiene mensajes y enlaces personales. No subirlo directamente a un repositorio, no reutilizar números, enlaces de invitación, credenciales, conversaciones ni identificadores en código o documentación pública.

## Mapa de ideas y responsables propuestos

| ID | Apartado fuente aproximado | Necesidad e instrucción para el equipo | Responsable candidato | Estado / condición |
|---|---|---|---|---|
| MAT-ARCH-001 | 1–55 | Arquitectura universal modular, bots/web/APIs/apps y dispositivos; documentar contratos y permisos por módulo | Docs, Base, System | Propuesta; mantener Base prioritario |
| MAT-ARCH-002 | 540–715 | Marketplace de **módulos de software** con instalación/firma/permisos/licencias; separado del comercio físico | Extensions, SDK, Marketplace | Diseño, no mezclar con ventas de hardware |
| MAT-ARCH-003 | 1900–2143 | Comunicaciones NetLive Morse y codificación: definir canal, límites físicos, tolerancia a fallos y pruebas en laboratorio | System / I+D | Investigación sin protocolo validado |
| MAT-ARCH-004 | 2146–2243 + PDF relevador | Control de cargas por placa/relevadores: someter esquema AC a ingeniería eléctrica profesional antes de construir o probar | System / I+D hardware | Prototipo no homologado |
| MAT-ARCH-005 | 2245–2400 + PDF Tri-Red | Seguridad Tri-Red: métricas de redes autorizadas, redundancia y políticas defensivas; nada de intrusión real | System / seguridad | Solo test autorizado/aislado |
| MAT-ARCH-006 | 2404–2574 | Sistema submarino SRSA: definición científica y médica, pruebas de fisiología, oxígeno/presión y certificaciones | I+D especializado | Alto riesgo; no apto para uso humano sin validación |
| MAT-ARCH-007 | 2575–2846 | NetLive Research Lab: robótica, visualización de conceptos y hardware avanzado; agrupar hipótesis y recursos | Docs / I+D / System | Investigación separada del comercio |
| MAT-ARCH-008 | 2847–4177 | Ciudad subterránea ultrarresistente: análisis geotécnico, ambiental, seguridad, viabilidad, costos y permisos | Docs / I+D civil | Visión lejana, no obra aprobada |
| MAT-ARCH-009 | 4178–4767 | Generador mecánico-magnético Halbach/rotor/bobinas: medir fuente primaria y balance energético neto bajo carga real | System / I+D energía | Experimental; no prometer energía ilimitada |
| MAT-ARCH-010 | 4787–5238 | Arquitectura integral del ecosistema: dependencias, versión, plugins, interfaces y servicio común sin acoplamiento | Base, API, SDK, Docs | Arquitectura, revisar conflictos con código real |
| MAT-ARCH-011 | 5239–5669 | AI Engine intercambiable: proveedores autenticados, licencias, sandbox, permisos y límites explícitos | AI, Vault, System | No adoptar proveedor por nombre o promesa |
| MAT-ARCH-012 | 5670–5979 | Control nativo de OS desde web/bots: interfaz con consentimiento por capacidad y protección de acceso remoto | System, App, Interfaces, Base | Privilegio mínimo, opt-in, auditoría |
| MAT-ARCH-013 | 5980–6222 | AutoAccept: automatización de invitaciones sin evitar verificación, autorización ni protecciones de grupos | Automation, WhatsApp; Bot futuro | Bloqueado hasta políticas y runtime |
| MAT-ARCH-014 | 6223–6439 | Menu Music Generator: contenido original o licenciado y compatibilidad de medios por plataforma; audio explícito | Interfaces, App, WhatsApp, Bot futuro | Derechos y cliente compatibles |
| MAT-ARCH-015 | 6440–~8780 | IA de personalidad e interfaz semántica universal: adaptar texto sin alterar autorización ni lógica interna | AI, Interfaces, System | Consentimiento, no ejecutar código de IA sin permisos |
| MAT-ARCH-016 | 8782–~11890 | Generador de bases, comandos, bloques, perfiles y extensibilidad; evaluar qué existe antes de crear duplicados | Base, SDK, Extensions | Plan de módulos, no sustituir núcleo Rust |
| MAT-ARCH-017 | 11894–12941 | Sticker System con versiones simples/avanzadas; respetar licencias, formatos y políticas del proveedor | App, WhatsApp; Bot futuro | No dar por listo si no hay tests |
| MAT-ARCH-018 | 12942–~14500 | Distributed Compute: dividir trabajo, checkpoints, colas, workers heterogéneos, aislamiento de tareas y reconciliación | Cloud, Server, Automation | No sumar RAM física de VPS como si fuera una sola |
| MAT-ARCH-019 | ~14500–15350 | MSEL — lenguaje/representación universal/localización; gramática, compilación, compatibilidad y seguridad | SDK, System, Extensions | I+D de compilador, separado de lenguaje humano |
| MAT-ARCH-020 | 15350–16971 | Modular Joint/robótica: servo, drive, freno, encoder y seguridad funcional, límites de torque y temperatura | System / I+D robótica | Equipo industrial, sin montaje no validado |
| MAT-ARCH-021 | Conversación del 19/11 | **Comercio físico Matterssmith**: venta propia/mayoreo, entrega $0 elegible, propietario/servicio, generación/logística | Marketplace, Vault, Web, App, API, Automation, System | Requisitos MAT-COM-001..018 documentados |

Las líneas son **rangos de navegación**, no citas de certificación. Se conservan rótulos de origen que pueden ser ideas especulativas y no proyectos financiados. Los documentos PDF aportan esquemas/hipótesis y no informes de seguridad ni cumplimiento.

## Reglas de priorización y no duplicación

1. **Actual:** Base-Matter y WhatsApp Rust, seguridad, roles y permisos. Bot-Matter bloqueado.
2. **Planificado/comercial:** los 18 requisitos MAT-COM detallados en [Marketplace-Matter](https://github.com/Matterssmith/Marketplace-Matter/blob/matter/docs/REQUISITOS_ECOSISTEMA_COMERCIO.md).
3. **I+D:** generador, relevadores, ciudad, respiración submarina, robótica y redes. Para cada uno exigir hipótesis falsable, prueba segura y responsable experto; no anunciar funcionamiento o fabricación.
4. **Plataforma futura:** AI Engine, SDK/MSEL, Distributed Compute, NetLive y plugins. Primero revisar herramientas existentes y evitar que una especificación antigua sobrescriba arquitectura Rust vigente.
5. **Producto final:** cada equipo aprobado podrá integrarse con la tienda, registro Vault y un contrato comercial revisado. No mezclar prototipo con producto disponible.

## Próxima tarea documental

Abrir expedientes técnicos independientes por familia cuando el propietario decida prioridades. No alterar Bot-Matter ni reescribir ejecutables desde este ZIP sin revisión de versiones. Resolver discrepancias de nombres históricos frente a los repos actuales antes de aprobar código.

Créditos:
Hecho por Lournyx Matterssmith [Lou-Nyx].
