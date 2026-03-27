# Departamento 7 — Sales & Business Development

> **AI%: 75%** | Nivel: Revenue | Dueño: CEO

---

## Contexto Crítico — Fase 0

> **Los fundadores reconocen no tener expertise en ventas.** Esto no es un problema — es un punto de partida honesto.
> La estrategia de ventas para la Fase 0 está diseñada específicamente para personas sin background comercial:
> - **Estructura sobre intuición:** Scripts, procesos y HubSpot reemplazan la "habilidad de vender"
> - **IA como segundo cerebro:** Claude ayuda a preparar cada conversación y propuesta
> - **Calidez sobre volumen:** Con 50+ ex-clientes, lo que funciona no es prospección fría sino reactivación honesta
> - **WhatsApp sobre LinkedIn:** El canal donde ya existe la relación primero, el formal después

---

## Misión
Generar ingresos nuevos de forma estructurada y predecible — con o sin experiencia previa en ventas — usando un CRM configurado (HubSpot), scripts probados, IA para personalización y foco en los clientes más cercanos antes que en prospección fría.

---

## Responsabilidades Core

- Prospección y generación de leads cualificados (ICP: vendedores Amazon europeos)
- Gestión del pipeline de ventas en CRM
- Outreach personalizado (email, LinkedIn, DMs)
- Discovery calls y demos de servicios
- Elaboración y envío de propuestas comerciales
- Cierre de contratos y onboarding handoff a Customer Success
- Identificación y desarrollo de partnerships (agencias, consultoras, influencers del sector)
- Análisis de mercado: nuevos servicios demandados, gaps de competencia

---

## Perfil de Cliente Ideal (ICP) — PrepCenter

| Criterio | Descripción |
|---|---|
| **Tipo** | Vendedor Amazon FBA que necesita externalizar su logística 3PL |
| **Mercado** | España principalmente, Europa (UK, DE, FR, IT) en expansión |
| **Volumen** | €10K-500K/mes en ventas Amazon |
| **Necesidad** | Logística 3PL, gestión de cuenta, sourcing, o formación |
| **Fase** | Establecido (no beginner) o en crecimiento activo |
| **Canal de acceso** | LinkedIn, comunidades Amazon, eventos sector, referrals |

---

## Roles

| Rol | Tipo | Responsabilidad |
|---|---|---|
| CEO / Head of Sales | Humano | Cierre de deals grandes, partnerships, estrategia comercial |
| SDR (Sales Dev Rep) | Humano (o externalizado) | Prospección, outreach, calificación de leads |
| Prospecting AI Agent | IA (Clay + Apollo + Claude) | Búsqueda, enriquecimiento de leads, personalización de mensajes |
| CRM Automation | IA (HubSpot AI) | Seguimiento automático, recordatorios, scoring de leads |
| Proposal Generator | IA (Claude API) | Borradores de propuestas personalizadas |

---

## Stack de Herramientas IA 2026

| Herramienta | Uso |
|---|---|
| **Clay** | Enriquecimiento de leads con datos de múltiples fuentes + IA personalización |
| **Apollo.io** | Base de datos de prospects, email sequences, contact finding |
| **HubSpot CRM** | Pipeline de ventas, deal tracking, automatización de seguimiento |
| **LinkedIn Sales Navigator** | Identificación de prospects, señales de compra |
| **Claude API** | Personalización masiva de emails, análisis de empresas, propuestas |
| **Loom** | Video personalizados para prospects de alto valor |
| **DocuSign / PandaDoc** | Contratos digitales con firma electrónica |
| **Notion** | Playbooks de ventas, scripts de call, objection handling |

---

## KPIs del Departamento

| KPI | Descripción | Objetivo | Frecuencia |
|---|---|---|---|
| Leads Generados / Mes | Nuevos leads cualificados que entran al pipeline | 30-50/mes | Mensual |
| Lead-to-Opportunity Rate | % de leads que avanzan a oportunidad real | >30% | Mensual |
| Opportunity-to-Close Rate | % de oportunidades que cierran | >25% | Mensual |
| Sales Cycle Length | Días promedio desde primer contacto hasta firma | <30 días | Mensual |
| ARR por Cliente Nuevo | Valor anual promedio de cada nuevo contrato | Maximizar | Por deal |
| Pipeline Value | Valor total de oportunidades en CRM | 3x objetivo mensual | Semanal |
| Churn de Ventas | Deals perdidos y motivos | <50% por precio | Mensual |

---

## Dependencias con Otros Departamentos

- **Recibe de:** Marketing (leads inbound, contenido de apoyo a ventas), Data Analytics (datos del mercado, case studies con resultados)
- **Entrega a:** Customer Success (handoff de nuevos clientes), Finance (contratos firmados para facturación)
- **Colabora con:** Amazon Channel + Operations (para preparar demos y propuestas realistas)

---

## Ventas sin Experiencia en Ventas — El Sistema que Reemplaza la Habilidad

> Los fundadores tienen expertise en logística y operaciones, no en ventas. Aquí está el sistema para que eso no sea una barrera.

### Antes de cada conversación de ventas — Prep con Claude (5 min)

Copiar y completar este prompt en Claude:

```
Voy a hablar con [nombre] de [empresa]. Vende en Amazon en la categoría [X].
Quiere información sobre nuestro servicio de PrepCenter / 3PL.
Su situación actual es: [lo que sé de ellos].

Ayúdame a:
1. Identificar las 3 preguntas clave que debo hacer para entender su problema
2. Los argumentos más relevantes para su situación específica
3. Las posibles objeciones y cómo responderlas
4. Una propuesta de próximos pasos concreta para cerrar en esta llamada
```

### Estructura de la Discovery Call (30 min)

```
0:00-5:00   — Contexto: "Cuéntame sobre tu negocio Amazon"
5:00-10:00  — Problema: "¿Cómo estás gestionando ahora la logística? ¿Qué no funciona?"
10:00-15:00 — Presentación: "Esto es lo que hacemos y cómo funciona"
15:00-20:00 — Fit: "Basándome en lo que me has contado, creo que podemos ayudarte con X"
20:00-25:00 — Propuesta: "El servicio para tu volumen costaría X/mes. ¿Empezamos?"
25:00-30:00 — Cierre o siguientes pasos
```

**Regla de cierre:** Al final de cada llamada, define siempre un siguiente paso concreto con fecha:
- "Te mando la propuesta hoy antes de las 18h"
- "¿Cuándo tienes 10 minutos para revisar la propuesta juntos? ¿Jueves a las 11h?"

---

## SOP Mínimo — Pipeline de Ventas

### Etapas del Pipeline (HubSpot)

```
Lead → Contactado → Llamada/Demo → Propuesta enviada → Negociación → Cerrado / Perdido
```

| Etapa | Criterio de Entrada | Acción | Tiempo Máximo |
|---|---|---|---|
| **Prospect** | Lead identificado como ICP | Enriquecimiento con Clay, primer mensaje | - |
| **Contacted** | Mensaje enviado | Seguimiento D+3 y D+7 | 7 días |
| **Qualified** | Ha respondido y tiene necesidad real | Agendar discovery call | 3 días |
| **Demo** | Discovery call completada | Enviar propuesta | 2 días |
| **Proposal** | Propuesta enviada | Seguimiento D+2, D+5 | 5 días |
| **Negotiation** | Ha pedido cambios o negociación | Resolver objeciones | 3 días |
| **Closed** | Contrato firmado | Handoff a CS | Inmediato |

### Proceso de Outreach IA-Asistido (Clay + Claude)
1. Definir segmento objetivo (ej: sellers FBA alemanes con >3 años en Amazon, categoría hogar)
2. Clay busca y enriquece leads: nombre, empresa, URL de Amazon, LinkedIn, email
3. Claude genera personalización: analiza la tienda Amazon del prospect, identifica oportunidades
4. Secuencia de emails en Apollo: D0 (intro personalizada) → D3 (follow-up valor) → D7 (último intento)
5. Leads que responden → SDR toma el control para calificación

---

## Servicios y Pricing (Referencia)

| Servicio | Modelo de Precio | Rango |
|---|---|---|
| 3PL / Fulfillment | Por unidad + almacenaje | Cotización |
| Amazon Account Management | Mensualidad fija + % de ventas | €500-2.000/mes |
| PPC Management | Mensualidad + % del ad spend | €300-1.000/mes |
| Listing Optimization (pack) | Por proyecto | €300-800 |
| Auditoría de Cuenta | Por proyecto | €200-500 |
| Sourcing | Por pedido o mensualidad | Cotización |
| Ax Mentory® (formación) | Programa grupal / 1-to-1 | €500-3.000 |
