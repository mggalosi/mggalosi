# 🏎️ Notificador de Fórmula 1

Workflow desarrollado en n8n que consulta automáticamente el calendario de Fórmula 1 y envía notificaciones por Telegram con los horarios del fin de semana convertidos a UTC-3.

El sistema detecta:
- weekends estándar,
- weekends Sprint,
- y semanas sin carrera.

---

## ⚙️ Flujo del workflow

```text
Schedule Trigger (jueves 23hs)
   ↓
Consulta calendario vía API
   ↓
¿Hay carrera este fin de semana?
   ├── GP estándar
   ├── Sprint weekend
   └── Sin carrera
   ↓
Construcción dinámica del mensaje
   ↓
Envío vía Telegram
```

---

## 📸 Capturas

<img src="../images/Notificador F1.jpg" width="1000"/>

---

## 🔧 Detalles técnicos

- Consulta automática del calendario mediante Jolpica API
- Conversión automática de horarios UTC → UTC-3
- Detección dinámica de weekends Sprint
- Workflow completamente autónomo
- Compatible con cualquier instancia de n8n

---

## 📲 Ejemplos de notificación

### GP estándar

```text
🏎️ Este fin de semana hay Gran Premio

📍 Gran Premio de España · Barcelona

🕐 Clasificación: sábado 16:00
🏁 Carrera: domingo 15:00
```

### Sin carrera

```text
🏎️ Este fin de semana no hay carrera

📍 Próxima fecha:
Gran Premio de Canadá · Montreal
```

---

## 🔄 Patrón reutilizable

El workflow implementa un patrón muy común en automatización:

```text
Consulta externa → lógica condicional → notificación automática
```

El mismo enfoque puede reutilizarse para:
- alertas operativas,
- monitoreo de APIs,
- vencimientos,
- disponibilidad de servicios,
- o recordatorios automáticos.

---

## 🛠️ Stack técnico

![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![Jolpica API](https://img.shields.io/badge/Jolpica_API-FF1801?style=flat&logo=formula1&logoColor=white)
![Telegram Bot](https://img.shields.io/badge/Telegram_Bot-26A5E4?style=flat&logo=telegram&logoColor=white)