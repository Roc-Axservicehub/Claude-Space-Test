# Diagnóstico MVP — Qué Salió Mal y Cómo Reconstruir

> **Para dos cofundadores que llevan 2 años con un MVP y están reconstruyendo desde cero.**
> Este documento no es una crítica — es un mapa de los patrones más comunes que destruyen MVPs de 2 personas, y el plan para no repetirlos.

---

## SITUACIÓN ACTUAL — Semana 0 (2026-03-27)

> **Leer antes que nada. Esto define las prioridades reales.**

| Indicador | Estado | Implicación |
|---|---|---|
| **Runway de caja** | ~30 días | Modo emergencia activo |
| **Rentabilidad** | Confirmada tras subida de PVP en PrepCenter | El modelo funciona. El problema es volumen y retención |
| **Clientes activos** | **7 clientes** (PrepCenter como core) | Base pequeña pero con upsell inmediato disponible |
| **MRR** | Variable según volumen procesado | No es fijo — depende de unidades en almacén |
| **Clientes perdidos (6 meses)** | **50+ clientes** por falta de comunicación y seguimiento | Este es el verdadero diagnóstico. No falta captación — falta retención |
| **Pipeline de ventas** | 4+ leads activos | Material para cerrar, pero sin CRM configurado se perderán igual |
| **Servicio core** | PrepCenter (recepción · almacenaje · prep · expedición) | El 80% de ingresos. Almacenaje tiene el margen más alto |
| **Servicio con mayor margen** | Almacenamiento | Solo asocia gasto de alquiler nave + fijos |
| **Demanda de upsell** | Los 7 clientes actuales piden los 5 servicios | Ingresos adicionales sin un solo cliente nuevo |
| **Herramientas disponibles** | HubSpot, Holded, Prepbusiness, Google Drive, WhatsApp | Instaladas pero mal usadas — especialmente HubSpot |
| **Gap de expertise** | Ventas y RRHH | Ningún fundador tiene background en estas áreas |
| **Recursos disponibles** | Tiempo personal de los 2 fundadores + Claude | Sin presupuesto para contratar |

### El Diagnóstico Real

> **No perdisteis 50 clientes porque el servicio fuera malo.**
> **Los perdisteis porque no teníais un sistema para mantenerlos.**

La diferencia entre los 7 clientes que siguen y los 50 que se fueron:
probablemente los 7 son los que insistieron más o los que tuvieron más paciencia.

### La Secuencia Correcta para las Próximas Semanas

```
HOY:               Configurar HubSpot (2h) — stop the bleeding
Semana 1:          Reactivar 10-15 ex-clientes (ya os conocen, más rápido que nuevos)
Semana 1-2:        Cerrar los 4+ leads activos
Semana 1-3:        Upsell a los 7 clientes actuales (piden los 5 servicios)
Semana 3-4:        Si hace falta más, LinkedIn outreach nuevos leads
Mes 2 en adelante: Estructurar, automatizar, contratar
```

> **El error que no debes cometer ahora:** Dedicar tiempo a estructurar departamentos o implementar herramientas ANTES de configurar HubSpot y contactar a los ex-clientes. La estructura sirve para escalar. Primero hay que parar la hemorragia.

**→ Plan de acción inmediato:** [00-emergency-30day-plan.md](./00-emergency-30day-plan.md)

---

## Parte 1 — Los 8 Errores Más Comunes en MVPs de 2 Personas

### Error 1: Todo en la cabeza, nada documentado
**Síntoma:** "Yo sé cómo funciona esto" / "Ya lo tenemos hablado"
**Consecuencia:** Imposible delegar, imposible escalar, imposible auditar qué falla.
**Solución:** SOP (Standard Operating Procedure) para cada proceso antes de ejecutarlo.

---

### Error 2: Roles difusos — los dos hacen de todo
**Síntoma:** Ambos cofundadores tocan ventas, operaciones, producto y soporte el mismo día.
**Consecuencia:** Nada se hace bien, todo se hace a medias. Sin especialización no hay excelencia.
**Solución:** Dividir la empresa en dos "dominios de responsabilidad" claros:
- **CEO** (Visión, Ventas, Relaciones, Estrategia)
- **COO** (Operaciones, Producto, Tecnología, Procesos)

Cada decisión tiene un dueño. Si los dos deben decidir, la decisión no se toma.

---

### Error 3: Sin métricas desde el día 1
**Síntoma:** "Las cosas van bien / van mal" — pero sin números que lo respalden.
**Consecuencia:** Decisiones basadas en sensaciones, no datos. No sabes qué optimizar.
**Solución:** Implementar tracking básico desde semana 1:
- Ingresos recurrentes (MRR)
- Leads entrantes vs. leads convertidos
- Churn de clientes
- Margen por servicio

---

### Error 4: Deuda técnica y de proceso acumulada
**Síntoma:** Soluciones rápidas ("parches") que se vuelven permanentes. Herramientas de trabajo en hojas de cálculo.
**Consecuencia:** Cada nueva funcionalidad o cliente cuesta el doble que el anterior. El sistema no escala.
**Solución:** Arquitectura primero, herramientas después. Elegir stack y no cambiarlo durante 12 meses.

---

### Error 5: Sin sistema de delegación (ni a humanos ni a IA)
**Síntoma:** "Lo hago yo porque es más rápido explicarlo que explicar cómo hacerlo."
**Consecuencia:** El negocio no puede crecer más allá de las horas de los fundadores.
**Solución:** Para cada proceso repetitivo:
1. Documentar (SOP)
2. Automatizar con IA si es posible
3. Delegar a persona si requiere juicio humano
4. Supervisar con métricas

---

### Error 6: Customer Success reactivo
**Síntoma:** Solo hablas con clientes cuando hay un problema.
**Consecuencia:** Churn silencioso. El cliente se va antes de que sepas que está insatisfecho.
**Solución:** Onboarding estructurado + check-ins proactivos cada 2-4 semanas. Dashboards automáticos de salud del cliente.

---

### Error 7: Ventas y marketing sin sistema
**Síntoma:** Los clientes llegan por referencias o por suerte. No hay pipeline predecible.
**Consecuencia:** Ingresos irregulares, incapacidad de planificar el crecimiento.
**Solución:** Pipeline de ventas documentado con etapas claras + al menos 1 canal de generación de leads activo y medido.

---

### Error 8: Construir el producto antes que el negocio
**Síntoma:** Invertir tiempo en el MVP técnico/operativo antes de validar quién lo compra y por qué.
**Consecuencia:** Producto/servicio excelente que nadie usa o no está alineado con lo que el mercado paga.
**Solución:** Primero, 10 conversaciones de ventas con el cliente ideal. Luego, construir.

---

## Parte 2 — Autopsia del MVP: Preguntas Clave

Antes de reconstruir, responde estas preguntas con honestidad:

### Sobre el Producto/Servicio
- [ ] ¿Cuál de nuestros 5 servicios genera el 80% de los ingresos?
- [ ] ¿Cuál servicio tiene el margen más alto?
- [ ] ¿Qué servicio tienen más clientes activos hoy?
- [ ] ¿Qué quieren comprar nuestros clientes que no les estamos dando?

### Sobre Clientes
- [ ] ¿Cuántos clientes activos tenemos hoy?
- [ ] ¿Cuál es nuestro MRR (ingresos recurrentes mensuales)?
- [ ] ¿Cuántos clientes hemos perdido en los últimos 6 meses y por qué?
- [ ] ¿Quién es exactamente nuestro cliente ideal (ICP)?

### Sobre Operaciones
- [ ] ¿Qué proceso nos consume más tiempo y podría automatizarse?
- [ ] ¿Dónde están los cuellos de botella que frenan la entrega a clientes?
- [ ] ¿Qué herramientas usamos actualmente y cuáles no usamos bien?

### Sobre el Equipo
- [ ] ¿Qué responsabilidades tiene cada cofundador de forma clara?
- [ ] ¿Cuáles son las áreas donde ninguno de los dos tiene expertise?
- [ ] ¿Qué necesitamos externalizar primero?

---

## Parte 3 — Plan de Reconstrucción: Checklist por Prioridad

### CRÍTICO — Antes de hacer cualquier otra cosa
- [ ] **Definir el servicio core:** Elegir 1-2 servicios en los que AX Holding Group sea el mejor. El resto, secundario.
- [ ] **Establecer roles:** CEO y COO con responsabilidades escritas. Sin solapamiento.
- [ ] **Implementar tracking básico:** MRR, CAC (coste de adquisición), churn, margen. En una hoja o en Metabase.
- [ ] **Documentar el proceso de entrega del servicio principal:** SOP completo paso a paso.

### ALTA PRIORIDAD — Semanas 1-4
- [ ] Configurar CRM (HubSpot gratuito mínimo) con todos los leads y clientes actuales
- [ ] Automatizar el reporte semanal de Amazon para todos los clientes (n8n / Make)
- [ ] Crear plantilla de onboarding para nuevos clientes (Notion + emails automáticos)
- [ ] Definir OKRs del trimestre: máximo 3 objetivos, máximo 3 KPIs por objetivo

### MEDIA PRIORIDAD — Semanas 5-12
- [ ] Lanzar 1 canal de marketing activo (LinkedIn outreach IA-asistido con Clay/Apollo)
- [ ] Implementar sistema de facturación y contratos automatizados (Holded/Xero + Docusign)
- [ ] Crear dashboard ejecutivo centralizado con KPIs en tiempo real
- [ ] Estructurar Ax Mentory® con curriculum documentado y plataforma elegida (Circle/Kajabi)
- [ ] Establecer proceso de QC con proveedores y scoring de fábricas

### LARGO PLAZO — Semanas 13-26
- [ ] Primera contratación o externalización (Customer Success o Operaciones)
- [ ] Sistema completo de Supply Chain con base de datos de proveedores y AI scoring
- [ ] Automatización completa de PPC para todos los clientes (Perpetua/Helium 10 AI)
- [ ] Expansión a nuevos mercados o servicios basada en datos (no en intuición)

---

## Parte 4 — Reglas de Oro para No Repetir los Errores

```
1. Si no está documentado, no existe.
2. Si no se mide, no se puede mejorar.
3. Si un proceso se hace más de 3 veces igual, se automatiza.
4. Si una decisión tarda más de 48h, hay un problema de ownership.
5. Construir para el cliente de hoy, no para el cliente imaginario del futuro.
6. La IA ejecuta. Los humanos deciden y supervisan.
7. Un servicio excelente > cinco servicios mediocres.
```

---

*Última actualización: 2026-03-27 | Parte del proyecto: [Ver mapa completo →](./README.md)*
