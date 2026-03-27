# Departamento 6 — Supply Chain & Sourcing

> **AI%: 80%** | Nivel: Core | Dueño: Supply Chain Manager

---

## Misión
Conectar a los clientes de AX Holding Group con los mejores fabricantes de la red de 400+ fábricas, gestionar el proceso de sourcing, negociación, control de calidad y primera milla logística — con IA optimizando la selección, evaluación y seguimiento de proveedores.

---

## Responsabilidades Core

- Sourcing de nuevos productos para clientes: búsqueda y selección de fábricas
- Gestión y actualización de la base de datos de 400+ proveedores
- Negociación de precios, MOQs (mínimos de pedido) y condiciones con fabricantes
- Coordinación de muestras: solicitud, envío, evaluación
- Control de calidad (QC) pre-embarque en fábrica
- Gestión de Purchase Orders (POs) con fábricas
- Coordinación de primera milla: fábrica → almacén AX (China o España)
- Evaluación y scoring de proveedores (calidad, cumplimiento, precio, comunicación)
- Gestión de disputas con proveedores

---

## Roles

| Rol | Tipo | Responsabilidad |
|---|---|---|
| Supply Chain Manager | Humano | Estrategia de sourcing, negociaciones clave, decisiones de proveedor |
| Sourcing Agent (China) | Humano (local o partner) | Comunicación directa con fábricas en chino, visitas in-situ |
| QC Inspector | Humano (freelance) | Inspecciones pre-embarque en fábrica |
| Sourcing AI Agent | IA (Alibaba AI + Claude) | Búsqueda inicial de proveedores, scoring, análisis de cotizaciones |
| PO Tracking Agent | IA (n8n) | Seguimiento automático de pedidos, alertas de retraso |

---

## Stack de Herramientas IA 2026

| Herramienta | Uso |
|---|---|
| **Alibaba / 1688 + AI Search** | Búsqueda de proveedores, verificación básica, cotizaciones |
| **Supplier Scoring AI (custom n8n + Claude)** | Scoring automático de proveedores según criterios definidos |
| **Notion** | Base de datos de proveedores, historial de pedidos, evaluaciones |
| **Visión por computadora** | QC automatizado con fotos (análisis de defectos en producción) |
| **n8n** | Automatización: seguimiento de POs, alertas de hitos, notificaciones |
| **Claude API** | Análisis de cotizaciones comparativas, redacción de emails a fábricas, traducción |
| **Google Sheets / Airtable** | Gestión de POs, tracking de muestras |
| **Trello / Notion** | Workflow de sourcing por cliente |

---

## KPIs del Departamento

| KPI | Descripción | Objetivo | Frecuencia |
|---|---|---|---|
| Lead Time de Sourcing | Días desde solicitud hasta confirmación de proveedor | <10 días | Por proyecto |
| Tasa de Aprobación de Muestras | % de muestras aprobadas en primer envío | >70% | Mensual |
| Ahorro vs. Precio Inicial | % de reducción de precio en negociación | >10% | Por PO |
| QC Pass Rate | % de lotes que pasan inspección sin problemas | >95% | Por embarque |
| On-Time Production | % de pedidos producidos en fecha pactada | >90% | Por PO |
| Proveedor Scorecard Average | Puntuación promedio de proveedores activos | >4/5 | Trimestral |

---

## Dependencias con Otros Departamentos

- **Recibe de:** Clientes vía Customer Success (briefings de producto a fabricar), Amazon Channel (qué vende bien, qué necesitan fabricar)
- **Entrega a:** Operations & Logistics (mercancía a almacén), Finance (facturas de proveedores, costes de PO)
- **Colabora con:** Creative Production (especificaciones de packaging, etiquetas), Customer Success (updates de estado de pedidos a clientes)

---

## SOP Mínimo — Proceso de Nuevo Sourcing

### Fase 1 — Briefing de Producto (Días 1-2)
1. Cliente proporciona ficha de producto: categoría, especificaciones, target precio, MOQ, plazo
2. Supply Chain Manager valida viabilidad y define estrategia de sourcing
3. Búsqueda inicial automatizada: Alibaba AI + 1688 → lista de 10-15 proveedores candidatos

### Fase 2 — Selección de Proveedores (Días 2-5)
1. AI scoring de proveedores: antigüedad, volumen, verificaciones, reviews, categoría
2. Selección de top 5 para contactar
3. Envío de RFQ (Request for Quotation) estandarizado a los 5 proveedores
4. Seguimiento automático con recordatorios si no responden en 48h

### Fase 3 — Evaluación de Cotizaciones (Días 5-8)
1. Claude API analiza cotizaciones: precio, MOQ, lead time, certificaciones, condiciones
2. Comparativa automática en tabla
3. Negociación con top 2-3 proveedores
4. Selección final y solicitud de muestra

### Fase 4 — Muestras y QC (Días 8-21)
1. Coordinación de envío de muestras al cliente
2. Cliente evalúa y da feedback estructurado (formulario)
3. Si aprobada → PO y producción
4. Inspección QC pre-embarque antes de salida de fábrica

### Fase 5 — Producción y Primera Milla
1. Seguimiento automático de hitos de producción (n8n alertas)
2. Coordinación con Operations para recepción en almacén
3. Documentación: factura comercial, packing list, certificados

---

## Base de Datos de Proveedores — Campos Mínimos

| Campo | Descripción |
|---|---|
| Nombre / Empresa | Razón social del proveedor |
| Categorías | Productos que fabrica |
| Ubicación | Ciudad, provincia, China |
| Contacto | Nombre, email, WeChat |
| Verificado | Sí/No + tipo (Alibaba Gold, visita, etc.) |
| Historial de Pedidos | Nº pedidos, volumen total |
| Scorecard | Puntuación 1-5 en calidad, precio, comunicación, puntualidad |
| Certificaciones | ISO, CE, FDA, etc. |
| Idiomas | Chino, Inglés, Español |
| Estado | Activo / Inactivo / Bloqueado |
