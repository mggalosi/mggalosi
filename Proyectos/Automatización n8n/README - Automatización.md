# ⚙️ Automatización con n8n

Colección de workflows de automatización desarrollados con n8n, integrando APIs, lógica de negocio e inteligencia artificial.

Los proyectos de esta carpeta exploran patrones comunes de automatización como:
- procesamiento automático de información,
- clasificación con IA,
- notificaciones,
- integraciones entre servicios,
- manejo de errores,
- y workflows reutilizables.

---

## 📁 Workflows

### 📧 Clasificador de Emails con IA

Workflow de clasificación automática de correos utilizando Gemini y Gmail API.

Cada email es analizado según:
- remitente,
- asunto,
- cuerpo del mensaje,
- y contexto general.

El sistema asigna:
- categoría,
- score de confianza,
- y fallback manual cuando la confianza es baja.

### 🛠️ Stack

![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white)
![Gmail API](https://img.shields.io/badge/Gmail_API-EA4335?style=flat&logo=gmail&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=flat&logo=googlesheets&logoColor=white)

### 📌 Decisiones de diseño

- Temperatura 0.1 para respuestas determinísticas
- Fallback automático cuando la confianza es menor a 0.7
- Manejo independiente de errores

→ [Ver workflow](./Clasificador%20Emails%20IA/)

---

### 🏎️ Notificador de Fórmula 1

Workflow de notificaciones automáticas utilizando datos de la API de Fórmula 1 y Telegram.

El flujo:
1. consulta el calendario de carreras,
2. detecta weekends estándar o Sprint,
3. aplica lógica de negocio,
4. y envía notificaciones automáticas.

### 🛠️ Stack

![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![Jolpica API](https://img.shields.io/badge/Jolpica_API-FF1801?style=flat&logo=formula1&logoColor=white)
![Telegram Bot](https://img.shields.io/badge/Telegram_Bot-26A5E4?style=flat&logo=telegram&logoColor=white)

### 🔄 Patrón reutilizable

El mismo patrón puede aplicarse a:
- alertas operativas,
- monitoreo de APIs,
- vencimientos,
- recordatorios automáticos,
- o sistemas de notificación internos.

→ [Ver workflow](./Notificador%20F1/)

---

## 🧩 Conceptos trabajados

- Automatización de procesos
- Integración de APIs
- AI Agents
- Manejo de errores
- Clasificación automática
- Notificaciones automáticas
- Diseño de workflows reutilizables