# Idea de equipo — Matterssmith Commerce

## Título oficial para compartir
**Matterssmith Commerce — Comercio propio, titularidad de tecnología y logística eléctrica**

### Visión
Crear un mercado de productos físicos Matter que permita ventas minoristas y mayoreo, con una interfaz original de catálogo y vídeos, transporte Matter a costo $0 para el comprador en rutas participantes, registro cifrado de titularidad y un programa de reparación de por vida sujeto a una póliza sostenible.

En paralelo se estudia un **generador mecánico-magnético experimental** como una posibilidad de investigación de energía para flota eléctrica. El rendimiento no está demostrado y ninguna operación logística dependerá de él hasta medirlo.

El equipo deberá distinguir el comercio físico del marketplace previo de **módulos de software**. También deberá mantener separado el proyecto de seguridad defensiva **Tri-Red Emergency** y el diagrama de relevadores como prototipos documentales, no como componentes de productos listos.

### Qué comunicar sin ambigüedad
- **Dirección solicitada por el propietario:** comercio, productos propios, rutas elegibles gratuitas, registro de propiedad, reparaciones, logística eléctrica.
- **Requisitos de ingeniería:** trazabilidad de SKU, precios y tarifas transparentes, registros Vault cifrados, consentimiento/transferencia verificados, seguridad de dispositivos y criterios de aceptación medibles.
- **Pendientes:** jurisdicción y cifras comerciales, cobertura real de garantía, productos piloto, homologaciones eléctricas, operación logística, pruebas energéticas.
- **No hay** tienda lanzada, política comercial vitalicia aprobada, generador validado ni flota en servicio.
- No trabajar en Bot-Matter hasta el desbloqueo definido para Base-Matter.

### Trabajo asignado por módulo

| Repo | Entrega futura requerida | IDs de referencia |
|---|---|---|
| Marketplace-Matter | Negocio y catálogo, rutas gratis elegibles, factura y garantía | COM-001,004,005,009,018 |
| Web-Matter / Interfaces-Matter | Tienda original y accesible; precio total visible; invitado | COM-002,003,004 |
| App-Matter | Registro voluntario de equipo, posventa, transferencia y servicio | COM-003,007,008,010 |
| Vault-Matter | Propiedad cifrada, identidades y decisiones autorizadas | COM-007,008,013 |
| API-Matter | Contratos mínimos y seguros entre servicios | COM-004,008,013,014 |
| Server-Matter / Cloud-Matter | Estado de órdenes, tracking, idempotencia y retención | COM-005,006,014 |
| Automation-Matter | Optimización logística, entregas, devoluciones y taller | COM-005,006,012 |
| System-Matter / I+D | Seguridad de control eléctrico y mediciones del generador | COM-011,012,015,016 |
| Base-Matter | Contratos neutrales; sin reglas comerciales en el núcleo | COM-013,017 |
| Bot-Matter | Integración futura, actualmente bloqueada | COM-017 |
| Docs-Matter | Índice, prioridades, evidencia, decisiones del equipo | COM-018 |

`COM-XXX` es abreviatura de `MAT-COM-XXX`; el documento normativo de requisitos es [este](https://github.com/Matterssmith/Marketplace-Matter/blob/matter/docs/REQUISITOS_ECOSISTEMA_COMERCIO.md). La [propuesta de equipo](https://github.com/Matterssmith/Marketplace-Matter/blob/matter/docs/PROPUESTA_EQUIPO_MATTER_COMMERCE.md) está en Marketplace-Matter.

### Agenda de validación del equipo

1. Elegir **un electrodoméstico o producto Matter piloto** y definir costo, inventario, seguridad y piezas.
2. Seleccionar **una zona de reparto** y modelar cuándo la empresa puede subsidiar el envío a $0.
3. Modelar **un escenario de reparación** dentro de 1, 5 y 10 años y una reserva de costos.
4. Diseñar **una transferencia de propiedad** entre compradores sin divulgar datos Vault.
5. Hacer pruebas separadas del generador y control eléctrico; documentar riesgos y energía neta.

**Regla editorial:** al implementar, registrar estado `proposed|approved|implemented|verified`, responsables y evidencias. El documento fuente `Proyecto-Matter.zip` puede contener contactos/links privados; no publicarlo automáticamente.

Créditos:
Hecho por Lournyx Matterssmith [Lou-Nyx].
