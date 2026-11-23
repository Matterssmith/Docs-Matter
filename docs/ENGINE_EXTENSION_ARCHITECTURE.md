# ADR 2026-11-23 — Nuevo núcleo Engine-Matter y extensiones externas

**Fuente:** orden explícita del propietario del ecosistema Matter (2026-11-23). **Estado:** decisión de arquitectura aprobada, implementación pendiente.

## Mapa oficial de responsabilidades

| Actual | Futuro | Función |
| --- | --- | --- |
| WhatsApp-Matter | **Engine-Matter** | Motor de sistemas Matter internos. No implementa WhatsApp, Telegram ni Discord |
| Telegram-Matter | **Extension-Matter** | Integración con redes sociales externas: WhatsApp, Telegram, Discord y futuras |
| Discord-Matter | Retiro después de respaldo | Código útil se migra al adaptador Discord de Extension-Matter antes de borrar |
| MSEL (privado) | MSEL | Lenguaje, compilador y toolchain oficial autónomo, prioridad P0 |
| carpeta Matter-MSEL | **Engine-Matter/Matter-MSEL/** | Host/integración del lenguaje dentro del motor, NO segundo compilador |
| Base-Matter | Sin cambio | Bibliotecas y contratos reutilizables sin dependencias circulares |
| Social-Matter | Sin cambio | Sistema Matter propio, cliente del Engine, no adaptador de terceros |
| Bot-Matter | Sin cambio | Extensión opcional todavía bloqueada |
| Extensions-Matter (plural) | Sin cambio | Módulos generales privados/Anti; diferente de Extension-Matter (singular) |

## Regla de dependencias

Engine consume contratos propios de Base y hospeda la integración Matter-MSEL sin copiar el código privado de MSEL. Engine ofrece un contrato de extensiones estable para conectores autorizados en Extension-Matter. Los servicios Matter (Social, System, AI, App) no deben depender de un protocolo externo. El núcleo debe ser funcional aunque Extension-Matter no se ejecute.

## Migración segura

1. Registrar SHAs, CI, historial Git, licencias, dependencias Cargo, rutas, servicios desplegados y respaldos de los repositorios actuales.
2. Preparar Engine-Matter sobre WhatsApp-Matter/alpha con `Matter-MSEL/`, `engine/` y `systems/`; conservar proveedores heredados solo temporalmente.
3. Preparar Extension-Matter sobre Telegram-Matter/alpha con `adapters/whatsapp/`, `adapters/telegram/`, `adapters/discord/` y contratos de transporte confiable.
4. Copiar/portar proveedores WhatsApp de `providers/whatsapp-rust/`, `providers/baileys/`, `providers/whatsmeow/`, `crates/whatsapp-contracts/` y bindings sin mover sesiones ni secretos. Verificar equivalencia de pruebas Linux/Windows.
5. Construir Engine sin proveedores externos, ejecutar tests Social-Matter y MSEL nativo, validar identidad/consentimiento, Vault, replay, aislamiento y autorización previa a cualquier envío.
6. Reemplazar proveedor activo en una ventana controlada, sin dos sockets compartiendo estado. Eliminar duplicados solo después de pruebas reales y rollback verificado.
7. Renombrar repositorios desde administración GitHub y actualizar URLs, workflows y documentación; retirar Discord-Matter solo con respaldo e inventario concluido.

## Limitaciones verificadas

Los árboles Git `alpha` inspeccionados no contenían una carpeta existente llamada `Matter-MSEL/` para mover. Se preparó el directorio destino en WhatsApp-Matter/alpha, no se copió código desconocido. El conector GitHub de esta sesión permite cambios de archivos pero no cambiar nombres ni borrar repositorios. Esta decisión no activa funcionalidades ni CI automáticamente.

Créditos:
Hecho por Lournyx Matterssmith [Lou-Nyx].
