# ⚙️ Automatización con n8n

Workflows de automatización de procesos que combinan integraciones con APIs, lógica de negocio e inteligencia artificial. Cada workflow está diseñado como una **arquitectura reutilizable**: las acciones específicas se reemplazan según el stack del cliente, pero la lógica central se mantiene.

---

## 📁 Workflows

### 📧 [Clasificador de emails con IA](./clasificador-emails-IA/)

**Stack:** n8n · Google Gemini · Gmail API · Google Sheets

Workflow de clasificación automática de correos entrantes usando un AI Agent con Gemini. Cada email se analiza por remitente, asunto y cuerpo, y se clasifica en cuatro categorías con un score de confianza asociado.

**Decisiones de diseño clave:**
- Temperatura 0.1 en el modelo para respuestas determinísticas en clasificación
- Fallback automático a `revisar_manual` cuando la confianza es menor a 0.7
- Error trigger independiente que no interrumpe el flujo principal

→ [Ver arquitectura y documentación](./clasificador-emails-IA/)

---

### 🏎️ [Notificador de F1](./notificador-F1/)

**Stack:** n8n · Jolpica API · Telegram Bot

Workflow personal que demuestra el patrón más común en automatización: **consultar fuente externa → aplicar lógica de negocio → disparar notificación**. Maneja weekends estándar y de Sprint.

**El mismo patrón puede aplicarse a:**
- Alertas de stock o vencimiento de insumos
- Avisos de vencimiento de contratos o paquetes
- Monitoreo de cambios en APIs o fuentes externas

→ [Ver arquitectura y documentación](./notificador-F1/)

---

## 🧩 Patrones reutilizables

Los workflows de esta carpeta no son soluciones cerradas — son **plantillas de arquitectura**. El valor está en la estructura, no en las acciones específicas. Al adaptar un workflow a un cliente nuevo, lo que cambia son los nodos de acción; la lógica de trigger, procesamiento y manejo de errores se mantiene.
