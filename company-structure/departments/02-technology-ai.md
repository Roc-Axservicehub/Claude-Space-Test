# Departamento 2 — Technology & AI

> **AI%: 90%** | Nivel: Core | Dueño: COO / CTO

---

## Misión
Diseñar, implementar y mantener la infraestructura tecnológica y los agentes de IA que potencian el 85% de las operaciones de AX Holding Group. Este departamento es el multiplicador de productividad de toda la empresa.

---

## Responsabilidades Core

- Arquitectura y mantenimiento del stack tecnológico
- Desarrollo e implementación de agentes IA para automatización de procesos
- Gestión de integraciones entre herramientas (CRM, WMS, Amazon APIs, etc.)
- Seguridad de datos y backups
- Creación y mantenimiento de pipelines de datos hacia Data & Analytics
- Evaluación y adopción de nuevas tecnologías y herramientas IA
- Soporte técnico interno

---

## Roles

| Rol | Tipo | Responsabilidad |
|---|---|---|
| Tech Lead / CTO | Humano | Decisiones de arquitectura, supervisión de stack, priorización técnica |
| AI Engineer (externo/freelance) | Humano | Desarrollo de agentes IA, automatizaciones complejas |
| Automation Agent | IA | Ejecución de flujos n8n/Make, monitoreo de integraciones |
| Code Assistant | IA (Claude/Copilot) | Desarrollo asistido, revisión de código, documentación técnica |

---

## Stack de Herramientas IA 2026

| Herramienta | Categoría | Uso |
|---|---|---|
| **n8n / Make** | Automatización | Orquestación de flujos entre todas las herramientas |
| **Claude API (Anthropic)** | Agentes IA | Agentes de procesamiento, análisis, generación de contenido |
| **GitHub Copilot / Cursor** | Desarrollo | Asistencia de código IA |
| **Supabase / PostgreSQL** | Base de datos | Almacenamiento de datos operativos |
| **Vercel / Railway** | Infraestructura | Hosting de herramientas internas |
| **Zapier** | Automatización ligera | Integraciones rápidas sin código |
| **Retool / Appsmith** | Internal tools | Dashboards y herramientas internas sin código |
| **OpenAI / Gemini API** | Modelos IA | Funciones específicas de visión, embeddings, audio |

---

## KPIs del Departamento

| KPI | Descripción | Frecuencia |
|---|---|---|
| Uptime de integraciones | % de tiempo activo de flujos automáticos | Semanal |
| Horas ahorradas por automatización | Horas humanas ahorradas por semana por IA | Mensual |
| Tiempo de resolución de bugs | Horas promedio para resolver incidencias técnicas | Mensual |
| Coste de infraestructura / MRR | % de ingresos gastados en herramientas y hosting | Mensual |
| Nº de procesos automatizados | Acumulado de procesos que ya no requieren acción manual | Mensual |

---

## Dependencias con Otros Departamentos

- **Recibe de:** Todos (requerimientos de automatización, integraciones necesarias)
- **Entrega a:** Todos (herramientas funcionando, datos disponibles, automatizaciones activas)
- **Relación clave con:** Data & Analytics (pipeline de datos), Operations (WMS/integraciones logísticas), Amazon Channel (API integrations)

---

## SOP Mínimo — Proceso de Nueva Automatización

1. **Solicitud:** Cualquier departamento documenta el proceso manual que quiere automatizar (input, output, frecuencia, tiempo actual)
2. **Evaluación:** Tech Lead revisa viabilidad y prioriza en backlog
3. **Construcción:** Se construye en n8n/Make con documentación
4. **Testing:** Prueba con datos reales durante 1 semana en paralelo al proceso manual
5. **Activación:** Se activa la automatización y se desactiva el proceso manual
6. **Monitoreo:** Alerta configurada para fallos, revisión mensual de rendimiento

---

## Prioridades de Automatización para AX Holding Group

**Alta prioridad (hacer primero):**
- Reportes automáticos de Amazon para todos los clientes (semanal)
- Alertas de salud de cuenta Amazon (monitoreo 24/7)
- Onboarding de nuevos clientes (emails + Notion tasks automáticos)
- Sincronización CRM ↔ facturación

**Media prioridad:**
- Dashboard de logística en tiempo real
- Scoring automático de proveedores
- Generación de propuestas de venta personalizadas con IA

**Largo plazo:**
- Agente IA de atención al cliente (primera línea)
- Optimización automática de PPC con reglas IA
- Sistema de previsión de demanda para 3PL
