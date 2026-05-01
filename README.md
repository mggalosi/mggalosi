# 📊 Flux DATA & IA — Portfolio técnico

👋 Mi nombre es **Matias Galosi**, soy Ingeniero Industrial con formación en Ciencia de Datos y Automatización. 

Trabajo con datos reales bajo la marca **Flux DATA & IA**: análisis de datos y automatización de procesos para empresas y emprendimientos que necesitan tomar decisiones con información real.

Este repositorio funciona como **portfolio técnico y profesional**, con proyectos enfocados en **problemas reales** y no en ejercicios académicos aislados.

---

## 🧠 Qué hago

Ayudo a organizaciones y emprendedores a:

- 📌 Entender qué está pasando con sus datos
- ⚙️ Detectar ineficiencias operativas y oportunidades de mejora
- 👥 Segmentar clientes por comportamiento, valor y riesgo de abandono
- 🤖 Automatizar procesos repetitivos conectando herramientas sin código
- ✅ Tomar decisiones con números, no con intuición

---

## 🔎 Cómo trabajo

Mi enfoque prioriza el **problema antes que la herramienta**.

1. 🧩 Entiendo el contexto y la pregunta de negocio
2. 🧹 Evalúo la calidad y las limitaciones de los datos
3. 📊 Analizo y modelo solo lo necesario
4. 🗣️ Comunico conclusiones en lenguaje claro y accionable

Cada proyecto termina con recomendaciones concretas — no con reportes para archivar.

---

## 🛠️ Herramientas

- 🐍 Python
- 🗄️ SQL
- 📊 PowerBi
- ⚙️ n8n
- 🌱 Git / GitHub

---

## 💼 Proyectos con clientes reales

### 🏋️ FORZA Centro de Entrenamiento — Diagnóstico operacional 2025
**Berisso, Buenos Aires · Entregado diciembre 2025**

Análisis integral de los datos operativos de un centro de entrenamiento durante enero–noviembre 2025. Fuente: plataforma de gestión CROSSFY.

**Datos trabajados:**
- 📋 13.107 registros de turnos
- 📦 1.610 paquetes de clases
- 👥 593 socios registrados

**Ejes de análisis:** comportamiento de demanda, segmentación de socios, eficiencia de uso de paquetes, ocupación por turno, preferencia de productos y retención por cohorte.

**🔎 Hallazgos principales:**
- El 27.8% de los turnos comprados se pierden por vencimiento sin usar (4.340 turnos en el año)
- Solo el 24% de los socios de la cohorte de apertura mantiene membresía activa 20 meses después
- Ocupación global del 47%: margen de crecimiento sin ampliar infraestructura
- 1 producto genera el 51% del volumen total de ventas
- 58 paquetes comprados y nunca usados

**✅ Recomendaciones entregadas:** contacto directo con los 46 socios en riesgo de abandono, rediseño del paquete de 20 turnos, redistribución de demanda hacia horarios con disponibilidad, y protocolo de datos obligatorios al momento del alta.

---

## ⚙️ Automatización con n8n

### 📧 Clasificador de emails con IA — Arquitectura de referencia
**Stack: n8n · Google Gemini · Gmail API · Google Sheets**

Workflow de clasificación automática de correos entrantes usando un AI Agent con Gemini. Cada email se analiza por remitente, asunto y cuerpo, y se clasifica en cuatro categorías (soporte técnico, consulta de ventas, reclamo, spam) con un score de confianza asociado.

**Decisiones de diseño:**
- 🌡️ Temperatura 0.1 en el modelo para garantizar respuestas determinísticas en clasificación
- 🔁 Fallback automático a `revisar_manual` cuando la confianza es menor a 0.7
- 📊 Todas las clasificaciones se registran en Google Sheets con timestamp, categoría y resumen
- 🚨 Error trigger independiente para notificar fallos del workflow sin interrumpir el flujo principal

El workflow está diseñado como arquitectura adaptable: las acciones por categoría se reemplazan según el stack del cliente — etiquetado en Gmail, notificación en Slack, creación de ticket en CRM, etc.

---

### 🏎️ Notificador de F1 — Extracción de información de la temporada + Notificación
**Stack: n8n · Jolpica API · Telegram Bot**

Workflow personal que demuestra el patrón de integración más común en automatización de procesos: consultar una fuente externa con schedule, aplicar lógica de negocio y disparar una notificación.

Cada jueves a las 23hs consulta el calendario de la temporada actual, detecta si hay carrera ese fin de semana, construye un mensaje con horarios convertidos a UTC-3 y lo envía por Telegram. Maneja weekends estándar y de Sprint, y notifica la próxima fecha cuando no hay actividad.

**El mismo patrón puede ser aplicado directamente a:**
- 📦 Alertas de stock o vencimiento de insumos
- 📄 Avisos de vencimiento de contratos o paquetes
- 📡 Monitoreo de cambios en APIs o fuentes externas

---

## 🔬 Proyectos de exploración técnica

Estos proyectos no tienen cliente — los uso para explorar herramientas y metodologías sobre datasets de dominio público. No los presento como trabajo comercial.

### 🏎️ Análisis de datos de Fórmula 1 (1950–2024)
Análisis exploratorio sobre resultados y rendimiento en competencias de F1.

**Hipótesis exploradas:**
1. Los pilotos que largan desde la pole position tienen mayor probabilidad de ganar la carrera
2. Los equipos con mayor presupuesto concentran la mayoría de los campeonatos en las últimas dos décadas
3. La cantidad de abandonos por carrera ha disminuido con el tiempo por mejoras en la fiabilidad

---

### ⛽ Análisis de precios de combustibles en Argentina (2016–2024)
Estudio de comportamiento de precios por tipo de combustible y por provincia. Incluye entrenamiento de modelo predictivo con machine learning.

**Hipótesis exploradas:**
1. Los precios presentan una tendencia creciente sostenida a lo largo de los años
2. Existe una brecha sistemática de precios entre provincias del interior y AMBA
3. La Nafta Premium muestra mayor variación relativa, mientras que el Gasoil común es más estable

---

## 🚀 Sobre este repositorio

Este repositorio irá creciendo con nuevos proyectos y mejoras sobre los existentes, manteniendo siempre el foco en **análisis de datos y automatización aplicados a problemas reales de negocio**.

📍 *Berisso, Buenos Aires — trabajo de forma remota con clientes de toda Argentina.*  
📬 *flux.data.ia.26@gmail.com*  
⛓️‍💥 LinkedIn: www.linkedin.com/in/mggalosi
