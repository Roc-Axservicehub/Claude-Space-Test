# Departamento 9 — Finance & Legal

> **AI%: 85%** | Nivel: Control | Dueño: COO / Gestor externo

---

## Misión
Mantener la salud financiera de AX Holding Group, asegurar el cumplimiento legal y fiscal, gestionar la facturación a clientes y pagos a proveedores — con máxima automatización para minimizar tiempo administrativo de los fundadores.

---

## Responsabilidades Core

- Facturación automática a clientes (recurrente y por proyecto)
- Control de cobros y gestión de impagados
- Pagos a proveedores y gestión de gastos
- Contabilidad y cierre mensual
- Cumplimiento fiscal: IVA, IRPF, IS (Impuesto de Sociedades)
- Contratos: redacción, revisión y archivo de contratos con clientes y proveedores
- Cash flow y previsión financiera
- Cumplimiento GDPR y protección de datos

---

## Roles

| Rol | Tipo | Responsabilidad |
|---|---|---|
| COO / Admin | Humano | Supervisión, aprobación de pagos, decisiones financieras |
| Gestor/Asesor Externo | Humano (externalizado) | Contabilidad oficial, declaraciones fiscales, compliance legal |
| Billing AI Agent | IA (n8n + Holded) | Generación y envío automático de facturas |
| Contract AI Assistant | IA (Claude API) | Borradores de contratos, revisión de cláusulas, traducciones |
| Expense Tracking | IA (Holded/Spendesk) | Categorización automática de gastos |

---

## Stack de Herramientas IA 2026

| Herramienta | Uso |
|---|---|
| **Holded** | ERP español: facturación, contabilidad, CRM básico, inventario |
| **Xero** (alternativa) | Contabilidad cloud, facturación internacional |
| **n8n / Make** | Automatización de facturación recurrente, recordatorios de pago |
| **DocuSign / Signaturit** | Firma electrónica de contratos (válida legalmente en España/EU) |
| **Claude API** | Redacción de contratos, análisis de cláusulas, Q&A legal |
| **Spendesk / Pleo** | Gestión de gastos de empresa con tarjetas virtuales |
| **Stripe / Redsys** | Cobro online: tarjeta, SEPA, recurrente |
| **Wise Business** | Pagos internacionales a proveedores (China, etc.) con bajas comisiones |

---

## KPIs del Departamento

| KPI | Descripción | Objetivo | Frecuencia |
|---|---|---|---|
| MRR (Monthly Recurring Revenue) | Ingresos recurrentes confirmados | Crecimiento mensual | Mensual |
| Días de Cobro Pendiente (DSO) | Media de días hasta cobro de facturas | <30 días | Mensual |
| Burn Rate | Gastos mensuales totales | Monitoreo vs. runway | Mensual |
| Runway | Meses de operación con el cash actual | >6 meses | Mensual |
| Margen Neto | (Ingresos - Gastos) / Ingresos | >20% | Mensual |
| Facturas Vencidas | Importe de facturas sin cobrar >30 días | <5% del MRR | Semanal |

---

## Dependencias con Otros Departamentos

- **Recibe de:** Sales (contratos cerrados para facturación), Customer Success (confirmaciones de renovación), Operations (costes de logística)
- **Entrega a:** Executive (P&L, runway, cash flow), Data Analytics (datos financieros para BI), todos (presupuestos aprobados)
- **Coordina:** Asesor externo para compliance fiscal

---

## SOP Mínimo — Ciclo de Facturación Mensual

### Facturación Recurrente (automatizada)
1. Día 1 del mes: Holded genera automáticamente todas las facturas recurrentes según contratos activos
2. Email automático enviado al cliente con la factura
3. Si pago domiciliado (SEPA): cobro automático el día 5
4. Si pago manual: recordatorio automático el día 10 si no se ha cobrado
5. Escalación a CS Manager si no se cobra antes del día 15

### Facturación por Proyecto (semi-automática)
1. CS / Ops confirma entrega del proyecto en sistema
2. n8n trigger: genera factura en Holded con datos del proyecto
3. Revisión rápida por COO (2 min) antes de envío
4. Envío y seguimiento de cobro

### Cierre Mensual
1. Día 5 del mes siguiente: asesor externo recibe acceso a Holded para cierre contable
2. Revisión de P&L con CEO+COO el día 10
3. Ajuste de previsión de cash flow y runway
4. Archivo de documentación fiscal

---

## Contratos Mínimos Necesarios

| Documento | Para qué | Herramienta |
|---|---|---|
| Contrato de Servicios (cliente) | Cada nuevo cliente | Plantilla + DocuSign |
| Contrato 3PL / Almacenaje | Clientes de logística | Plantilla + DocuSign |
| NDA (Non-Disclosure Agreement) | Nuevas relaciones comerciales | Plantilla + DocuSign |
| Contrato con Proveedor | Fábricas y proveedores clave | Plantilla + firma digital |
| Política de Privacidad / GDPR | Web y servicios | Abogado externo |
| Términos y Condiciones | Web y Ax Mentory® | Abogado externo |

---

## Estructura de Costes de Referencia

| Categoría | Tipo | % Estimado de Gastos |
|---|---|---|
| Personal / Freelancers | Variable | 40-50% |
| Herramientas y Software | Fijo | 10-15% |
| Logística / Almacén | Variable | 15-20% |
| Marketing y Publicidad | Variable | 5-10% |
| Asesoría Legal/Fiscal | Fijo | 3-5% |
| Otros operativos | Variable | 5-10% |
