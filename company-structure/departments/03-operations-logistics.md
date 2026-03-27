# Departamento 3 — Operations & Logistics

> **AI%: 85%** | Nivel: Core | Dueño: COO

---

## Misión
Gestionar las operaciones de logística 3PL de AX Holding Group: recepción de mercancía, almacenamiento en China y España, preparación de pedidos (prep center), envío a Amazon FBA y gestión de incidencias logísticas, con el máximo nivel de automatización posible.

---

## Responsabilidades Core

- Recepción e inspección de mercancía en almacenes (China / España)
- Gestión de inventario en tiempo real
- Preparación de pedidos (labeling, bundling, packaging según estándares Amazon)
- Coordinación de envíos marítimos y aéreos
- Gestión de proveedores logísticos (couriers, transitarios, aduanas)
- Tracking de envíos y comunicación de estado a clientes
- Resolución de incidencias: mercancía dañada, pérdidas, retrasos
- Cumplimiento de requisitos de Amazon FBA (dimensiones, etiquetas, restricciones)

---

## Roles

| Rol | Tipo | Responsabilidad |
|---|---|---|
| Operations Manager | Humano | Supervisión general, decisiones sobre incidencias, relación con proveedores |
| Warehouse Staff | Humano | Manipulación física de mercancía, preparación de pedidos |
| Logistics AI Agent | IA | Tracking automático, alertas de stock, generación de shipping plans |
| WMS System | IA/Software | Gestión de inventario, órdenes de trabajo, trazabilidad |

---

## Stack de Herramientas IA 2026

| Herramienta | Uso |
|---|---|
| **WMS (Linnworks / Ware2Go / propio)** | Gestión de almacén, inventario, órdenes |
| **Shipbob / Flexport** | Fulfillment y logística internacional con IA |
| **n8n / Make** | Automatización: tracking → cliente, alertas de stock bajo, shipping plans |
| **Amazon Seller Central API** | Generación automática de shipment plans hacia FBA |
| **Slack / Telegram bots** | Alertas en tiempo real de incidencias logísticas |
| **Google Sheets / Airtable** | Tracking manual de operaciones especiales |
| **Visión por computadora** | Inspección de QC automatizada en recepción (largo plazo) |

---

## KPIs del Departamento

| KPI | Descripción | Objetivo | Frecuencia |
|---|---|---|---|
| On-Time Delivery Rate | % de envíos entregados en fecha prometida | >95% | Semanal |
| Order Processing Time | Horas desde recepción hasta preparación lista | <24h | Diario |
| Inventory Accuracy | % de discrepancias entre stock físico y sistema | <1% | Mensual |
| Coste por Unidad Preparada | Coste operativo / unidades procesadas | Minimizar | Mensual |
| Tasa de Incidencias | % de pedidos con problema logístico | <2% | Mensual |
| Lead Time Promedio | Días desde fábrica hasta almacén Amazon | Monitoreo | Por envío |

---

## Dependencias con Otros Departamentos

- **Recibe de:** Supply Chain (mercancía e información de proveedores), Amazon Channel (shipping plans, volumen previsto), Clientes vía Customer Success
- **Entrega a:** Amazon Channel (confirmación de FBA enviado), Customer Success (tracking updates), Data & Analytics (datos de costes y tiempos)
- **Colabora con:** Finance (facturación de servicios 3PL a clientes), Technology (WMS integrations)

---

## SOP Mínimo — Ciclo de Operación 3PL

### Entrada de Mercancía
1. Cliente notifica envío entrante con POL (Purchase Order List) → automático via formulario
2. WMS genera Advance Shipping Notice (ASN)
3. Recepción física: conteo, inspección, foto de evidencia
4. Sistema actualiza inventario en tiempo real
5. Notificación automática al cliente: "Tu mercancía ha llegado"

### Preparación y Envío FBA
1. Cliente aprueba shipping plan en Amazon Seller Central
2. Sistema genera picking list y trabajo para almacén
3. Prep: etiquetado FNSKU, packaging, bundling según especificaciones
4. Generación automática de documentos de envío (packing list, factura comercial)
5. Booking con transitario / courier
6. Tracking compartido automáticamente con cliente

### Cierre
1. Confirmación de entrega en centro Amazon
2. Facturación automática del servicio al cliente
3. Actualización de KPIs en dashboard

---

## Estándares Amazon FBA (Referencia Rápida)

- Etiquetas FNSKU en cada unidad (no código de barras del fabricante)
- Cajas máximo 50 lbs / dimensiones según categoría de producto
- Suffocation warning en bolsas plásticas >5 pulgadas
- Expiration dates visibles si aplica
- Sin precio del proveedor visible en el producto
