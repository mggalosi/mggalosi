# 🏋️ FORZA Centro de Entrenamiento — Diagnóstico operacional 2025

**Cliente:** FORZA Centro de Entrenamiento · Berisso, Buenos Aires
**Período analizado:** Enero – Noviembre 2025
**Entregado:** Diciembre 2025
**Fuente de datos:** Plataforma de gestión CROSSFY

---

## 🎯 Contexto y objetivo

FORZA es un centro de entrenamiento en Berisso, Buenos Aires, con aproximadamente 20 meses de operación al momento del análisis. El dueño necesitaba entender el comportamiento real de sus socios y su operación a partir de los datos que acumuló la plataforma de gestión durante el año.

El objetivo fue generar un diagnóstico integral que respondiera preguntas concretas: ¿cuándo va la gente? ¿qué paquetes funcionan y cuáles no? ¿quiénes están por irse? ¿cuánto se pierde en turnos vencidos sin usar?

---

## 📦 Datos trabajados

| Archivo | Período | Registros |
|---|---|---|
| Turnos (`turnos_2025_unificado.xlsx`) | Ene–Nov 2025 | 13.107 filas |
| Paquetes (`paquetes_2025_unificado.xlsx`) | Ene–Nov 2025 | 1.610 filas |
| Socios (`listadoDeUsuarios.xls`) | Descarga dic 2025 | 593 socios |

---

## 🔎 Ejes de análisis

El análisis se estructuró en seis ejes temáticos:

1. **Comportamiento de demanda** — patrones horarios, días de la semana, estacionalidad y ausentismo
2. **Segmentación de socios** — clasificación en 5 segmentos según actividad reciente y antigüedad
3. **Eficiencia de paquetes** — tasa de aprovechamiento por tipo de paquete y pérdidas por vencimiento
4. **Ocupación por turno** — heatmap de ocupación y ranking de slots más y menos concurridos
5. **Preferencia de paquetes** — participación de mercado por tipo de combo y evolución mensual
6. **Base de socios** — evolución de altas y retención por cohorte de alta

---

## 🔎 Hallazgos principales

### Demanda
- El pico de demanda se concentra en **9h–10h** y en la franja nocturna **19h–20h**
- Los **jueves** son el día más concurrido de la semana
- El turno de **16h** es el menos concurrido de forma consistente en todos los días
- El sábado tiene actividad solo entre las 9h y las 11h

### Socios
- **35% de los socios con historial puede considerarse inactivo** (sin paquete hace más de 90 días)
- El 20% de los socios más activos genera el **53% de todos los turnos del año**
- Los socios inactivos promediaron solo 2 paquetes antes de abandonar — se fueron antes de generar el hábito
- **187 socios están registrados pero nunca compraron un paquete**

### Paquetes
- El **27.8% de los turnos comprados se pierde por vencimiento** — 4.340 turnos en el año
- El paquete de 20 turnos tiene solo un **48% de uso promedio** y deja en promedio 10 turnos sin usar
- **58 paquetes fueron comprados y nunca usados** (0 turnos asistidos al vencimiento)
- Básquet EDB tiene una tasa de uso del **30%**: el formato mensual no se adapta a esa disciplina

### Ocupación
- La ocupación global promedio es del **47%** — margen de crecimiento sin ampliar infraestructura
- El paquete de 12 turnos de Semi Personalizado representa el **51% de todos los paquetes vendidos**

### Retención
- De la cohorte de apertura (abril 2024), solo el **24% mantiene paquete activo 20 meses después**
- Los primeros 3 meses son críticos: los socios que no consolidan el hábito en ese período tienen alta probabilidad de abandono

---

## ✅ Recomendaciones entregadas

**Operación:**
- Gestión activa de los turnos nocturnos (19h–20h) con lista de espera e incentivos para redistribuir hacia franjas con disponibilidad
- Comunicación proactiva de horarios con capacidad libre

**Retención:**
- Contacto directo y personalizado con los **46 socios "En riesgo"** (sin paquete hace 31–90 días)
- Programa de acompañamiento para socios nuevos: bienvenida en el primer turno + check-in al mes + incentivo en la renovación del tercer paquete

**Oferta de paquetes:**
- Rediseño del paquete de 20 turnos: rollover de turnos sobrantes, conversión a trimestral o discontinuación
- Reformulación del paquete de Básquet EDB: clases individuales o paquete bimestral
- Mini-paquete de bienvenida (3–4 clases) para socios nuevos

**Calidad de datos:**
- Hacer obligatorios al alta: fecha de nacimiento, contacto de emergencia y apto médico
- Protocolo de datos mínimos para que los análisis futuros sean más precisos

---

## 🛠️ Stack técnico

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=flat&logo=python&logoColor=white)

---

## 📄 Entregable

El análisis fue presentado como informe en PDF de 15 páginas con todas las visualizaciones y el detalle de cada eje. El informe fue entregado directamente al dueño del gimnasio.
