# Departamento 12 — Data & Analytics

> **AI%: 95%** | Nivel: Transversal | Dueño: COO / Data Lead

---

## Misión
Centralizar todos los datos de AX Holding Group en un único sistema de inteligencia, proporcionar KPIs en tiempo real a todos los departamentos, detectar patrones, predecir problemas y habilitar decisiones basadas en datos — siendo el sistema nervioso de toda la empresa.

---

## Responsabilidades Core

- Centralización de datos de todos los sistemas (Amazon SP-API, CRM, WMS, finanzas)
- Diseño y mantenimiento de dashboards ejecutivos y operativos
- Definición y tracking de KPIs por departamento
- Alertas automáticas cuando métricas salen de rangos esperados
- Análisis ad-hoc para decisiones estratégicas
- Modelos predictivos: demanda, riesgo de churn, rendimiento de clientes
- Data governance: calidad, privacidad y acceso a datos
- Reporting a cofundadores: P&L, crecimiento, salud del negocio

---

## Roles

| Rol | Tipo | Responsabilidad |
|---|---|---|
| COO / Data Owner | Humano | Definición de métricas, decisiones sobre arquitectura de datos |
| Data Analyst | Humano (part-time o freelance) | Análisis complejos, modelos predictivos, data quality |
| BI AI Agent | IA (Metabase AI + Claude) | Generación de insights automáticos, respuestas a preguntas en lenguaje natural |
| ETL Pipeline | IA/Automatización (n8n + dbt) | Extracción, transformación y carga de datos desde todas las fuentes |
| Alert Agent | IA (n8n) | Monitoreo continuo y alertas cuando KPIs salen de rango |

---

## Stack de Herramientas IA 2026

| Herramienta | Categoría | Uso |
|---|---|---|
| **Metabase AI** | BI / Dashboards | Dashboards self-service, preguntas en lenguaje natural |
| **dbt (Data Build Tool)** | Transformación de datos | Modelos de datos limpios y documentados |
| **BigQuery / Supabase** | Data Warehouse | Almacenamiento centralizado de todos los datos |
| **n8n / Airbyte** | ETL / Integración | Pipelines de datos desde fuentes externas |
| **Claude API** | Análisis IA | Análisis de datos en lenguaje natural, generación de insights |
| **Looker Studio** | Reporting | Dashboards compartibles con clientes (opcionales) |
| **Amazon SP-API** | Fuente de datos | Datos de ventas, inventario, PPC en tiempo real |
| **HubSpot API** | Fuente de datos | Pipeline de ventas, datos de clientes |
| **Holded API** | Fuente de datos | Datos financieros, facturas, cobros |

---

## KPIs del Departamento (Meta-KPIs)

| KPI | Descripción | Objetivo | Frecuencia |
|---|---|---|---|
| Data Freshness | % de dashboards con datos actualizados en <24h | 100% | Diario |
| Data Accuracy | % de discrepancias detectadas en datos | <1% | Semanal |
| Dashboard Adoption | % de departamentos que usan activamente sus dashboards | >80% | Mensual |
| Alert Response Time | Tiempo entre alerta disparada y acción tomada | <4h | Por incidencia |
| Insights Actionables/Mes | Nº de insights de datos que llevan a una acción concreta | >5/mes | Mensual |

---

## Arquitectura de Datos — Mapa de Fuentes

```
FUENTES DE DATOS
    │
    ├── Amazon SP-API ──────────────────────────────┐
    ├── HubSpot CRM ────────────────────────────────┤
    ├── Holded (Finance) ───────────────────────────┤
    ├── WMS / Logística ───────────────────────────┤──▶ n8n/Airbyte ──▶ BigQuery ──▶ dbt ──▶ Metabase AI
    ├── Helium 10 / PPC tools ────────────────────┤
    ├── Circle / LMS (Ax Mentory®) ───────────────┤
    └── Google Analytics (web) ─────────────────────┘
```

---

## Dashboards Prioritarios

### Dashboard Ejecutivo (CEO + COO)
Actualización: diaria | Vista: semana/mes/trimestre

| Métrica | Fuente |
|---|---|
| MRR actual y tendencia | Holded |
| Nº clientes activos y churn | HubSpot |
| Pipeline de ventas (valor total) | HubSpot |
| Cash en banco y runway | Holded |
| Salud promedio de cartera (CS) | HubSpot |
| Top 5 clientes por ingresos | Holded + HubSpot |

### Dashboard Amazon Channel
Actualización: diaria | Por cuenta de cliente

| Métrica | Fuente |
|---|---|
| Ventas totales / BSR | Amazon SP-API |
| ACoS / TACoS / ROAS | Amazon Ads API |
| Inventario disponible FBA | Amazon SP-API |
| Account Health Score | Amazon SP-API |
| Ranking de keywords objetivo | Helium 10 |

### Dashboard Operaciones
Actualización: diaria

| Métrica | Fuente |
|---|---|
| Pedidos pendientes de procesar | WMS |
| Stock por cliente en almacén | WMS |
| Envíos en tránsito | WMS + courier API |
| Incidencias abiertas | WMS |

### Dashboard Ventas & Marketing
Actualización: semanal

| Métrica | Fuente |
|---|---|
| Leads nuevos / semana | HubSpot |
| Conversión por etapa de pipeline | HubSpot |
| CAC (coste de adquisición) | Holded + HubSpot |
| Tráfico web y leads inbound | Google Analytics |

---

## Dependencias con Otros Departamentos

- **Recibe de:** Todos los departamentos (datos de sus sistemas y operaciones)
- **Entrega a:** Executive (dashboard ejecutivo), Todos (KPIs y alertas propias de su área)
- **Rol único:** Es el único departamento que tiene visión completa de la empresa

---

## SOP Mínimo — Implementación de Nuevo KPI

1. **Solicitud:** Departamento define la métrica que necesita medir (nombre, fórmula, frecuencia, acción si sale mal)
2. **Validación:** Data Lead confirma que los datos existen y son fiables
3. **Pipeline:** Se construye o ajusta el ETL para traer ese dato a BigQuery
4. **Modelo dbt:** Se crea el modelo limpio y documentado
5. **Dashboard:** Se añade la visualización en Metabase
6. **Alerta:** Se configura n8n para alertar si el KPI sale del rango esperado
7. **Documentación:** Se registra en el catálogo de KPIs de la empresa (Notion)

---

## Principio Fundamental

> **"En AX Holding Group, ninguna decisión importante se toma sin un dato que la respalde."**
>
> El objetivo de Data & Analytics no es crear reportes bonitos — es cambiar comportamientos y decisiones en todos los departamentos.
