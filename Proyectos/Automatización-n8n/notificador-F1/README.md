# 🏎️ Notificador de F1 — Integración API + Telegram

**Stack:** ![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white) ![Jolpica API](https://img.shields.io/badge/Jolpica_API-FF1801?style=flat&logo=formula1&logoColor=white) ![Telegram Bot](https://img.shields.io/badge/Telegram_Bot-26A5E4?style=flat&logo=telegram&logoColor=white)
**Tipo:** Workflow personal · Patrón de integración reutilizable

---

## 🎯 Qué hace

Cada jueves a las 23hs consulta el calendario de la temporada actual de Fórmula 1, detecta si hay carrera ese fin de semana, construye un mensaje con los horarios convertidos a UTC-3 y lo envía por Telegram. Maneja weekends estándar y de Sprint, y notifica la próxima fecha cuando no hay actividad ese fin de semana.

---

## 🔎 Cómo funciona

```
Schedule Trigger (jueves 23hs)
   ↓
Jolpica API → calendario de la temporada actual
   ↓
¿Hay carrera este fin de semana?
   ├── Sí (GP estándar) → Construye mensaje con horarios en UTC-3
   ├── Sí (Sprint weekend) → Construye mensaje con horarios de Sprint + Carrera
   └── No → Busca la próxima fecha + construye mensaje informativo
   ↓
Telegram Bot → envío del mensaje
```

---

## 💡 Por qué este workflow importa más allá de F1

El flujo implementa el **patrón de integración más frecuente en automatización de procesos de negocio:**

> Consultar fuente externa con schedule → aplicar lógica condicional → disparar notificación

Este mismo patrón puede aplicarse directamente a:

| Caso de uso | Fuente | Notificación |
|---|---|---|
| Alerta de stock bajo | ERP / Google Sheets | WhatsApp / Slack |
| Vencimiento de contratos | CRM / Notion | Email / Telegram |
| Vencimiento de paquetes de clientes | Sistema de gestión | WhatsApp |
| Cambios en tipo de cambio o precios | API financiera | Telegram / Email |
| Monitoreo de disponibilidad de un servicio | HTTP Request | Slack |

---

## 🔧 Detalles técnicos

- **API:** [Jolpica F1 API](https://api.jolpi.ca/ergast/f1/) — wrapper gratuito de la API histórica de Ergast
- **Conversión horaria:** los horarios de la API vienen en UTC. El workflow los convierte automáticamente a UTC-3 (Argentina) antes de armar el mensaje
- **Lógica de Sprint:** los weekends de Sprint tienen un cronograma distinto (Sprint Qualifying + Sprint Race + Qualifying + Race). El workflow detecta el tipo de fin de semana y construye el mensaje correspondiente
- **Sin dependencias externas:** funciona en cualquier instancia de n8n con acceso a internet

---

## 📄 Formato del mensaje generado

**GP estándar:**
```
🏎️ Este fin de semana hay Gran Premio

📍 Gran Premio de España · Barcelona
📅 Sábado 31 de mayo

🕐 Clasificación: sábado 16:00 (ARG)
🏁 Carrera: domingo 15:00 (ARG)
```

**Sin carrera:**
```
🏎️ Este fin de semana no hay carrera

Próxima fecha:
📍 Gran Premio de Canadá · Montreal
📅 Fin de semana del 13 de junio
```
