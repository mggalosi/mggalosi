# 📧 Clasificador de Emails con IA

Workflow desarrollado en n8n para clasificar automáticamente correos entrantes utilizando Gemini y Gmail API.

El sistema analiza cada email y determina:
- categoría,
- nivel de confianza,
- y flujo de derivación correspondiente.

---

## 🎯 Problema

Equipos con alto volumen de emails suelen mezclar:
- soporte técnico,
- ventas,
- reclamos,
- spam,
- y consultas generales.

La clasificación manual consume tiempo, genera inconsistencias y dificulta la escalabilidad operativa.

---

## ⚙️ Flujo del workflow

```text
Gmail Trigger
   ↓
Extracción de asunto + remitente + cuerpo
   ↓
AI Agent (Gemini)
   ↓
Clasificación + score de confianza
   ↓
¿Confianza >= 0.7?
   ├── Sí → Derivación automática
   └── No → Revisión manual
   ↓
Registro en Google Sheets
```

---

## 📂 Categorías

| Categoría | Descripción |
|---|---|
| soporte_tecnico | Problemas o consultas técnicas |
| consulta_ventas | Interés comercial |
| reclamo | Quejas o devoluciones |
| spam | Correos irrelevantes |
| revisar_manual | Baja confianza del modelo |

---

## 🧠 Decisiones de diseño

### Temperatura 0.1

Se priorizó consistencia y determinismo en las respuestas del modelo para minimizar variabilidad en la clasificación.

### Fallback manual

Cuando la confianza es menor a 0.7, el email se deriva automáticamente a revisión humana para evitar clasificaciones erróneas.

### Error handling desacoplado

Los errores del workflow se manejan mediante un Error Trigger independiente, evitando que una falla bloquee el procesamiento del resto de los emails.

### Logging y trazabilidad

Cada clasificación queda registrada con:
- timestamp,
- categoría,
- score,
- y resumen generado.

---

## 📌 Ejemplo

| Input | Output |
|---|---|
| "No puedo ingresar a mi cuenta" | `soporte_tecnico` — 0.94 |
| "Quiero información sobre precios" | `consulta_ventas` — 0.91 |
| "Solicito devolución del pago" | `reclamo` — 0.89 |

---

## 🛠️ Stack

![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat&logo=googlegemini&logoColor=white)
![Gmail API](https://img.shields.io/badge/Gmail_API-EA4335?style=flat&logo=gmail&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=flat&logo=googlesheets&logoColor=white)

---

## 📸 Capturas

<img src="../images/Clasificador Emails.jpg" width="1000"/>

---

## 🔄 Posibles adaptaciones

El workflow puede integrarse fácilmente con:
- Slack
- HubSpot
- Pipedrive
- Notion
- CRMs internos
- Sistemas de tickets