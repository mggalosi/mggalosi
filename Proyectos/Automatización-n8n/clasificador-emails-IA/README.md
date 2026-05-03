# 📧 Clasificador de emails con IA

**Stack:** ![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white) ![Google Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white) ![Gmail API](https://img.shields.io/badge/Gmail_API-EA4335?style=flat&logo=gmail&logoColor=white) ![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=flat&logo=googlesheets&logoColor=white)
**Tipo:** Arquitectura de referencia (adaptable a cualquier cliente)

---

## 🎯 Problema que resuelve

Las bandejas de entrada de equipos con alto volumen de consultas (soporte técnico, ventas, atención al cliente) mezclan tipos de mensajes muy distintos que requieren respuestas y flujos diferentes. Clasificar a mano es lento, inconsistente y no escala.

Este workflow automatiza la clasificación de cada email entrante, la registra con trazabilidad completa y deriva el mensaje al flujo correcto según su categoría.

---

## 🔎 Cómo funciona

```
Gmail (trigger)
   ↓
Extrae: remitente · asunto · cuerpo
   ↓
AI Agent (Gemini)
   ↓
Clasificación + score de confianza
   ↓
¿Confianza >= 0.7?
   ├── Sí → Acción por categoría (etiqueta / Slack / CRM / etc.)
   └── No → Cola "revisar_manual"
   ↓
Registro en Google Sheets (timestamp · categoría · resumen)
```

**Error Trigger independiente:** si cualquier nodo falla, se ejecuta un flujo separado de notificación sin interrumpir el procesamiento de los demás emails.

---

## 📂 Categorías de clasificación

| Categoría | Descripción |
|---|---|
| `soporte_tecnico` | Consultas sobre uso del producto o fallas |
| `consulta_ventas` | Interés en compra, precios o planes |
| `reclamo` | Quejas o solicitudes de devolución |
| `spam` | Correos sin relevancia comercial |
| `revisar_manual` | Confianza < 0.7 — requiere revisión humana |

---

## 🔧 Decisiones de diseño

**Temperatura 0.1 en Gemini:** la clasificación requiere respuestas determinísticas y consistentes. Una temperatura alta introduce variabilidad innecesaria que reduce la confiabilidad del sistema.

**Fallback explícito:** cuando el modelo no alcanza el umbral de confianza, el email se deriva a revisión manual en lugar de asignarse a una categoría con baja certeza. Esto evita errores costosos en la respuesta al cliente.

**Error trigger independiente:** los fallos del workflow no bloquean el procesamiento del resto de los emails. El trigger de error notifica el fallo (por email o Slack) y sigue ejecutándose de forma desacoplada.

**Registro con timestamp:** todas las clasificaciones quedan en Google Sheets con fecha, categoría, score y resumen. Esto permite auditar el comportamiento del sistema y detectar categorías con alta tasa de revisión manual.

---

## 🔄 Cómo adaptar este workflow a un cliente

Las acciones por categoría son los únicos nodos que cambian. Ejemplos de adaptación:

| Canal del cliente | Acción de derivación |
|---|---|
| Gmail | Agregar etiqueta + mover a carpeta |
| Slack | Enviar mensaje al canal correspondiente |
| CRM (HubSpot, Pipedrive) | Crear tarea o ticket automático |
| Notion | Crear entrada en base de datos |

El resto de la arquitectura (trigger, clasificación con IA, fallback, registro) se reutiliza sin cambios.
