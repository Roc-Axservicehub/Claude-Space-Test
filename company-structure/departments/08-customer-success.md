# Departamento 8 — Customer Success

> **AI%: 80%** | Nivel: Retención | Dueño: CS Lead / COO

---

## Por Qué Este Departamento Es el Más Crítico de Toda la Empresa

> **Dato real:** AX Holding Group perdió 50+ clientes en 6 meses. No por servicio deficiente — por falta de comunicación, seguimiento y registro de actividad.
>
> Customer Success no es un departamento "nice to have". Es el departamento que determina si la empresa sobrevive.
> Con 7 clientes activos hoy y 50+ que se fueron, **retener es más urgente que captar.**

### El Ciclo de la Hemorragia (cómo se perdieron los 50 clientes)

```
Cliente entra → Se le hace el servicio → Nadie registra la relación →
Surge un problema o pregunta → Nadie responde a tiempo →
Cliente se siente ignorado → Se va sin avisar →
Nadie lo nota hasta que deja de pagar
```

### Cómo romper el ciclo (hoy, con lo que tenéis)

```
Cliente entra → Se registra en HubSpot ese mismo día →
Check-in automático semanal (n8n + WhatsApp/email) →
Alerta si no responde en 72h → Contacto proactivo →
Cliente se siente atendido → Renueva y compra más servicios
```

---

## Misión
Garantizar que cada uno de los 7 clientes activos recibe atención proactiva, que los 50+ ex-clientes reciben una oportunidad de reactivación, y que ningún cliente futuro se pierde por falta de seguimiento — usando HubSpot y automatizaciones básicas como primera capa de sistema.

---

## Responsabilidades Core

- Onboarding estructurado de nuevos clientes
- Gestión de la relación mensual con cada cliente activo
- Reporting periódico de resultados (automatizado + análisis humano)
- Identificación de riesgos de churn y acciones preventivas
- Gestión de incidencias y escalaciones
- Upselling y cross-selling de servicios adicionales
- Recogida de feedback y NPS
- Coordinación interna: ser el puente entre el cliente y los departamentos operativos

---

## Roles

| Rol | Tipo | Responsabilidad |
|---|---|---|
| CS Manager / Account Manager | Humano | Relación estratégica, decisiones de escalación, upselling |
| CS Analyst | Humano | Análisis de resultados, preparación de reportes complejos |
| Reporting AI Agent | IA (n8n + Claude + SP-API) | Generación automática de reportes semanales/mensuales |
| Support AI Bot | IA (Intercom AI) | Primera línea de soporte: preguntas frecuentes, status updates |
| Health Score Monitor | IA (n8n) | Alerta automática cuando un cliente entra en zona de riesgo |

---

## Stack de Herramientas IA 2026

| Herramienta | Uso |
|---|---|
| **Intercom AI** | Chat de soporte con IA, ticketing, knowledge base |
| **n8n / Make** | Automatización de reportes, alertas de salud, onboarding flows |
| **Claude API** | Análisis de datos de cliente, generación de insights en reportes |
| **Notion** | Portal del cliente, SOPs de CS, base de conocimiento interna |
| **HubSpot** | Tracking de health score, historial de interacciones, tareas de CS |
| **Loom** | Video-reportes personalizados para clientes estratégicos |
| **Google Data Studio / Metabase** | Dashboards de resultados por cliente |
| **Typeform / Tally** | Encuestas NPS y feedback trimestral |

---

## KPIs del Departamento

| KPI | Descripción | Objetivo | Frecuencia |
|---|---|---|---|
| Churn Rate | % de clientes que cancelan al mes | <3% | Mensual |
| NPS (Net Promoter Score) | Puntuación de recomendación (0-10) | >50 | Trimestral |
| Time to Value (TTV) | Días desde contrato hasta primer resultado medible | <30 días | Por cliente |
| Expansion Revenue | % de ingresos de upsells a clientes existentes | >20% del MRR | Mensual |
| Response Time | Tiempo promedio de respuesta a cliente | <4h (laborable) | Semanal |
| Health Score Promedio | Puntuación de salud de cartera de clientes | >75/100 | Mensual |
| CSAT | Customer Satisfaction Score en soporte | >85% | Mensual |

---

## Customer Health Score — Modelo PrepCenter

| Factor | Peso | Verde | Amarillo | Rojo |
|---|---|---|---|---|
| **Volumen enviado este mes** | 30% | ≥ mes anterior | -20% | -50% o sin envíos |
| **Responde a comunicaciones** | 25% | En <24h | En 1-3 días | No responde o >3 días |
| **Tiempo sin contacto proactivo nuestro** | 20% | <7 días | 7-14 días | >14 días |
| **Facturación al día** | 15% | Al corriente | 1 factura pte. | >1 factura pte. |
| **Servicios adicionales activos** | 10% | 2+ servicios | 1 servicio extra | Solo PrepCenter |

**Acción automática (n8n):**
- **Verde:** Check-in semanal automático (WhatsApp/email) + reporte mensual
- **Amarillo:** Alerta al Fundador A → llamada proactiva en 48h máximo
- **Rojo:** Escalación urgente → llamada ese mismo día + plan de recuperación

> **Señal de alarma más importante:** Si un cliente no envía stock durante 2 semanas sin aviso previo, está en riesgo de irse. Contactar inmediatamente.

---

## Dependencias con Otros Departamentos

- **Recibe de:** Sales (handoff de nuevos clientes), Amazon Channel (datos de rendimiento), Operations (estado de logística)
- **Entrega a:** Sales (señales de upsell, referidos), Data Analytics (datos de churn y salud), Finance (confirmación de renovaciones)
- **Coordina:** Entre cliente y todos los departamentos operativos

---

## SOP Mínimo — Onboarding de Nuevo Cliente

### Semana 1 — Configuración
**Día 1:**
- Email automático de bienvenida con acceso al portal Notion del cliente
- CS Manager envía Loom de bienvenida (2 min)
- Formulario de kick-off: objetivos, productos, accesos necesarios (Amazon, etc.)

**Día 3:**
- Kick-off call (30-45 min): objetivos, expectativas, proceso de trabajo, puntos de contacto
- Configuración de accesos: Amazon, sistemas AX, canal de comunicación (Slack/WhatsApp)

**Día 5:**
- Primer análisis de cuenta entregado (auditoría rápida + quick wins identificados)
- Plan de 30/60/90 días enviado al cliente

### Semana 2-4 — Activación
- Implementación de cambios acordados
- Check-in semanal de 15 min (o actualización por escrito)
- Reporte automático de primeros datos

### Mes 1 — Cierre de Onboarding
- Business Review: resultados del primer mes vs. objetivos
- Ajuste de estrategia si necesario
- Transición a modo de gestión mensual estándar

---

## SOP Mínimo — Gestión Mensual de Cliente

**Automático (IA):**
- Reporte mensual generado automáticamente el día 1 del mes siguiente
- Datos: ventas, PPC performance, inventario, incidencias resueltas

**Humano:**
- CS Manager revisa y añade análisis e insights estratégicos (15 min/cliente)
- Envío con comentario personalizado

**Monthly Business Review (trimestralmente):**
- Call de 30-45 min para revisar objetivos, resultados y plan siguiente trimestre
