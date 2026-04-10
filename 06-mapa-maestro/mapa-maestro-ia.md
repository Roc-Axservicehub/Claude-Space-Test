# Mapa Maestro de IA — Ax Holding Group
> Versión 1.0 — Abril 2026 | Documento vivo. Actualizar con cada sesión de arquitectura.

---

## 1. Estructura corporativa

### Equipo actual
| Persona | Rol | Área principal |
|---|---|---|
| Roc | Co-founder, CEO | Estrategia, ventas, producto, tech |
| Leander | Co-founder | Operaciones, gestión, todo lo demás |
| Juan | Operario de almacén | Ejecución física de servicios Prepcenter |

### Verticales del grupo
| Vertical | Estado | Prioridad IA |
|---|---|---|
| **Ax Prepcenter** | Activo, creciendo | 🔴 Inmediata |
| **Ax Agency** | Pausado (0 clientes) | 🟡 Fase 2 |
| **Ax Design** | Limitado (MVP fallido) | 🟡 Fase 2 |
| **Ax Website** | Mínimo (1 cliente) | 🟡 Fase 2 |
| **Ax Mentory** | Planificado | 🟢 Fase 3 |

---

## 2. Stack de herramientas actual

### Herramientas activas
| Herramienta | Categoría | Estado | Integrada con IA |
|---|---|---|---|
| HubSpot | CRM | ✅ Activo | ✅ Conectado Cowork |
| Prepbusiness (WMS/SGA) | Operaciones | ✅ Activo | ❌ Sin integración |
| Holded | ERP / Contabilidad | ✅ Activo | ❌ Sin integración |
| Stripe | Pagos | ✅ Activo | ❌ Sin integración |
| Wise | Banca | ✅ Activo | ❌ Sin integración |
| Google Workspace | Productividad | ✅ Activo | ❌ Sin integración |
| WhatsApp | Comunicación | ✅ Activo | ❌ Sin integración |
| Canva | Diseño | ✅ Activo | ❌ Sin integración |
| Adobe | Diseño avanzado | ✅ Activo | ❌ Sin integración |
| Eleven Labs | Voz / Audio | ✅ Activo | ❌ Sin integración |
| Instagram | RRSS | ⚠️ Abandonado | ❌ Sin integración |
| LinkedIn (Roc + Leander) | RRSS | ⚠️ Mínimo | ❌ Sin integración |
| LinkedIn (Ax page) | Marca | ⚠️ Abandonado | ❌ Sin integración |
| Web (HubSpot CMS) | Presencia | ⚠️ Básica | ❌ Sin integración |
| Apollo | Prospección | ✅ Conectado | ✅ Conectado Cowork |
| Make.com | Automatización | ✅ Conectado | ✅ Conectado Cowork |
| Claude (Cowork) | IA central | ✅ Activo | ✅ Este espacio |

---

## 3. Ax Prepcenter — Proceso actual (estado real)

### Ciclo completo de un cliente

```
CAPTACIÓN
  └── Formulario web / reserva videocall
        ↓
VENTAS (Roc/Leander)
  └── Prospecting manual → llamada → cierre
        ↓
ONBOARDING
  └── Setup cuenta WMS (Prepbusiness)
  └── Vinculación Seller Central Amazon
  └── Onboarding fee: 500€ (Stripe)
        ↓
OPERACIÓN ACTIVA
  Cliente crea órdenes en WMS
        ↓
EJECUCIÓN (Juan)
  └── Ve panel WMS → ejecuta manualmente
  └── ⚠️ SIN trazabilidad interna
  └── ⚠️ SIN notificaciones al cliente
  └── Cuando termina: añade tag en WMS
        ↓
FACTURACIÓN
  └── Día 19 de cada mes
  └── Factura generada en WMS → Stripe → cargo automático tarjeta
```

### Cuellos de botella identificados (críticos)
1. **Operaciones sin trazabilidad** — Juan trabaja sin sistema. Si escala el volumen, el proceso colapsa.
2. **Comunicación reactiva** — el cliente no recibe notificaciones proactivas del estado de sus órdenes.
3. **Roc y Leander como cuello de botella único** — todo pasa por ellos. Sin delegación real.
4. **Cashflow tardío** — cobro el día 19, servicios prestados durante todo el mes.
5. **Onboardings pendientes de cobro** — 5 × 500€ = 2.500€ sin cobrar.

---

## 4. Canales de presencia actual

| Canal | Estado | Seguidores/Visibilidad | Acción IA prioritaria |
|---|---|---|---|
| Web (HubSpot CMS) | Básica, desactualizada | — | Rebuild con aprobación social |
| Instagram @ax | Abandonada | ~200 | Activar con contenido IA |
| LinkedIn Roc | Mínimo | — | Estrategia de contenido personal |
| LinkedIn Leander | Mínimo | — | Estrategia de contenido personal |
| LinkedIn Ax page | Abandonada | — | Activar como canal B2B |
| WhatsApp | Canal principal cliente | — | Integrar en CRM |

---

## 5. Mapa de departamentos y agentes IA

### PRIORIDAD 1 — Operaciones Prepcenter 🔴
**Problema:** Juan trabaja sin trazabilidad. El proceso manual no escala.
**Objetivo IA:** visibilidad total del almacén, notificaciones automáticas al cliente, reducir carga de Roc/Leander en supervisión operativa.

| Agente / Herramienta | Función | Stack |
|---|---|---|
| **Agente Operaciones** | Monitoriza órdenes WMS, alerta a Juan, notifica al cliente | Prepbusiness API + WhatsApp/Email + Make.com |
| **Dashboard operativo** | Panel en tiempo real: órdenes pendientes, en proceso, completadas | Prepbusiness + HTML dashboard |
| **Agente de notificaciones** | Confirma recepción de stock, avisa cuando orden está lista | Make.com + WhatsApp Business |

**Repo:** `operaciones-prepcenter`

---

### PRIORIDAD 2 — Finanzas y Cobros 🔴
**Problema:** cashflow negativo, onboardings pendientes, sin visibilidad financiera integrada.
**Objetivo IA:** cobros automáticos, conciliación Holded+Stripe, alertas de impago, dashboard financiero.

| Agente / Herramienta | Función | Stack |
|---|---|---|
| **Agente Cobros** | Detecta onboardings sin cobrar, genera alerta, envía reminder | Holded API + Stripe + Make.com |
| **Dashboard financiero** | P&L en tiempo real, burn rate vs ingresos, forecast | Holded + Wise + Google Sheets |
| **Agente Conciliación** | Cruza facturas Holded con pagos Stripe automáticamente | Holded + Stripe + Make.com |

**Repo:** `finanzas-ax`

---

### PRIORIDAD 3 — Ventas y CRM 🟠
**Estado:** parcialmente construido. HubSpot conectado, plugin ventas-prepcenter creado.
**Objetivo IA:** gestionar inbound de agencias + Qogita + web, pipeline sin fricción, outreach sistematizado.

| Agente / Herramienta | Función | Stack |
|---|---|---|
| **gestionar-pipeline** ✅ | Revisión HubSpot, urgencias, acciones | HubSpot MCP |
| **prospectar-sellers** ✅ | Búsqueda leads Amazon sellers | Apollo + agent-prospector |
| **outreach-prepcenter** ✅ | Email frío + LinkedIn personalizado | Claude + templates |
| **preparar-llamada** ✅ | Briefing pre-call | HubSpot + Claude |
| **Agente inbound** | Cualifica leads entrantes de web automáticamente | HubSpot + Make.com |

**Repo:** `ventas-prepcenter` ✅ (creado)

---

### PRIORIDAD 4 — Marketing y Marca 🟠
**Estado:** presencia mínima, todo abandonado.
**Objetivo IA:** activar Instagram + LinkedIn con contenido consistente, construir brand voice Ax, mejorar web con aprobación social.

| Agente / Herramienta | Función | Stack |
|---|---|---|
| **Agente de contenido** | Genera posts Instagram + LinkedIn según brand voice | Claude + Canva + Make.com |
| **Brand Voice Ax** | Guía de voz y tono para todo el contenido | brand-voice skills |
| **Agente Web** | Actualiza copy web, gestiona formularios, aprobación social | HubSpot CMS + Claude |
| **Agente LinkedIn** | Estrategia de contenido personal Roc + Leander | LinkedIn + Claude |
| **Agente reputación** | Monitoriza menciones, reviews Amazon, respuestas | Make.com + web search |

**Repo:** `marketing-ax`

---

### PRIORIDAD 5 — Customer Success 🟡
**Estado:** no existe como función. El cliente se gestiona reactivamente.
**Objetivo IA:** proactividad con clientes, detección de churn, expansión de cuenta.

| Agente / Herramienta | Función | Stack |
|---|---|---|
| **Agente CS** | Revisa actividad clientes, detecta inactividad, dispara check-in | Prepbusiness + HubSpot + Make.com |
| **NPS automático** | Encuesta satisfacción post-onboarding y mensual | Make.com + Typeform |
| **Agente expansión** | Detecta clientes listos para ampliar servicios | HubSpot + Claude |

**Repo:** `customer-success-ax`

---

### PRIORIDAD 6 — Otros verticales (Fase 2-3) 🟢

**Ax Agency** — repo: `agencia-ax`
- Agente de propuestas, agente de reporting para clientes, gestión de proyectos IA

**Ax Design** — repo: `design-ax`
- Portfolio IA, brief automático, sistema de producción con trazabilidad

**Ax Website** — repo: `website-ax`
- Agente de proyectos web, entrega de assets, gestión de revisiones

**Ax Mentory** — repo: `mentory-ax`
- Agente de onboarding estudiantes, contenido del curso, soporte IA

---

## 6. Arquitectura de conexión entre departamentos

```
                    ROC (control total)
                          │
              ┌───────────┴───────────┐
              │     PANEL MAESTRO     │
              │  (dashboard central)  │
              └───────────┬───────────┘
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
   OPERACIONES        FINANZAS          VENTAS/CRM
   (Prepbusiness)    (Holded+Stripe)   (HubSpot)
        │                 │                 │
        └─────────────────┼─────────────────┘
                          │
                     MAKE.COM
                  (capa de integración)
                          │
              ┌───────────┴───────────┐
              │                       │
          MARKETING              CUSTOMER
         (contenido)              SUCCESS
```

**Make.com es la columna vertebral de integración.** Conecta todos los sistemas entre sí sin necesidad de código personalizado.

---

## 7. Roadmap de construcción

### Fase 1 — Estabilizar (Meses 1-2)
**Objetivo: parar la hemorragia operativa y financiera**

- [ ] Cobrar los 5 onboardings pendientes (2.500€)
- [ ] Agente operaciones: trazabilidad de órdenes Juan + notificaciones cliente
- [ ] Agente cobros: alertas de impago + conciliación Holded/Stripe
- [ ] Pipeline ventas activo: gestionar inbound agencias + Qogita correctamente
- [ ] HubSpot write access: desconectar y reconectar para permisos completos

### Fase 2 — Escalar (Meses 3-4)
**Objetivo: absorber el volumen de Qogita y partners sin colapsar**

- [ ] Dashboard operativo en tiempo real
- [ ] Agente inbound: cualificación automática de leads web
- [ ] Brand voice Ax definido
- [ ] Instagram y LinkedIn activados con contenido semanal IA
- [ ] Sistema de onboarding automatizado (WMS + Stripe + notificaciones)

### Fase 3 — Expandir (Meses 5-8)
**Objetivo: activar otros verticales con base sólida en Prepcenter**

- [ ] Customer Success sistematizado
- [ ] Ax Agency reactivado con infraestructura IA
- [ ] Panel central de supervisión de todos los departamentos
- [ ] Agentes de los otros verticales construidos y testados

### Fase 4 — Orquestar (Mes 9+)
**Objetivo: empresa que opera de forma semi-autónoma bajo dirección de Roc**

- [ ] Agente orquestador entre departamentos
- [ ] Dashboard maestro con visión completa del grupo
- [ ] Sistema de reporting automático semanal
- [ ] Ax Mentory lanzado

---

## 8. Próxima acción inmediata

**Esta semana, en orden:**

1. Cobrar los 5 onboardings pendientes → ¿están en HubSpot? ¿en Holded?
2. Construir agente de operaciones (trazabilidad Juan) → mayor impacto inmediato
3. Resolver HubSpot write access → sin esto el CRM está cojo
4. Activar LinkedIn de Roc con 2 posts/semana → captación orgánica B2B

---

*Documento generado con Asistente Dev-IA — Ax Holding Group*
*Próxima revisión: cuando se complete Fase 1*
