# 🏎️ Análisis Histórico de Fórmula 1 (1950–2024)
### Dashboard interactivo en Power BI

**Proyecto Final — Data Analytics**
**Autor:** Galosi Matias Gabriel &nbsp;|&nbsp; **Institución:** CODERHOUSE &nbsp;|&nbsp; **Año:** 2025

---

## 📋 Descripción

Dashboard interactivo desarrollado en **Power BI** que analiza más de **70 años** de historia del Campeonato Mundial de Fórmula 1, desde la primera temporada en 1950 hasta 2024.

El proyecto explora:
- 🏆 La evolución del rendimiento de pilotos y escuderías a lo largo de las décadas
- 🚦 El impacto de la posición de largada en el resultado final
- 🔧 La fiabilidad mecánica y tendencia de abandonos a través del tiempo
- ⏱️ El análisis estratégico de los pit stops

---

## 🔬 Hipótesis Analizadas

| # | Hipótesis | Resultado |
|---|-----------|-----------|
| **H1** | Los pilotos que largan desde la pole position tienen mayor probabilidad de ganar | ✅ **Confirmada** — los porcentajes de victoria desde pole son significativamente elevados en la mayoría de los circuitos |
| **H2** | Las escuderías con mayor presupuesto (Ferrari, Mercedes, Red Bull) dominan los campeonatos de las últimas dos décadas | ✅ **Confirmada** — estas tres escuderías y pilotos como Hamilton, Vettel y Verstappen concentran la mayor cantidad de títulos |
| **H3** | La cantidad de abandonos por carrera ha disminuido con el tiempo por mejoras tecnológicas | ✅ **Confirmada** — se evidencia una tendencia decreciente sostenida en retiros, especialmente en las últimas décadas |

---

## 🧭 Metodología

El análisis siguió un enfoque de **cuatro niveles**:

| Nivel | Tipo | Descripción |
|-------|------|-------------|
| 1️⃣ | **Descriptivo** | Exploración de métricas clave: victorias, podios, poles, abandonos y distribución por piloto, equipo y país |
| 2️⃣ | **Diagnóstico** | Análisis de correlaciones entre posición de largada, nacionalidad, escudería y resultado final |
| 3️⃣ | **Predictivo** | Modelos de regresión y series temporales para estimar puntos y evolución de métricas históricas |
| 4️⃣ | **Prescriptivo** | Recomendaciones basadas en combinaciones piloto–equipo–circuito con mayor tasa de éxito histórica |

---

## 🗃️ Modelo de Datos

El modelo relacional integra **14 tablas** conectadas en Power BI:

> Carreras · Circuitos · Pilotos · Escuderías · Resultados · Clasificaciones · Clasificación Pilotos · Clasificación Escuderías · Paradas Boxes · Resultados Sprints · Tiempos Vuelta · Resultados Escuderías · Temporadas · Estados

📊 **Volumen:** más de **20.000 registros** distribuidos entre las tablas.

---

## 📐 Medidas DAX Desarrolladas

Entre las principales medidas calculadas se destacan:

- 📉 Promedio y total de abandonos por carrera
- 💥 Total de accidentes
- ⚡ Vuelta más rápida por circuito
- 🥇 Cantidad de podios y carreras ganadas
- 📍 Porcentaje de victorias desde pole position
- 🔢 Victorias por posición de largada
- 👤 Top pilotos y top escuderías

---

## 📊 Páginas del Dashboard

| Página | Descripción |
|--------|-------------|
| 🖼️ **Portada** | Presentación visual del proyecto |
| 📑 **Índice & Glosario** | Guía de navegación y definición de términos |
| 📈 **General** | KPIs globales del campeonato |
| 🚦 **Salida desde Pole** | Análisis del impacto de la posición de largada |
| 🏅 **Pilotos & Escuderías** | Rankings históricos y evolución por décadas |
| 📉 **Evolución de Abandonos** | Tendencia de retiros a lo largo del tiempo |
| 🔧 **Pit Stops** | Análisis de paradas en boxes desde 2011 (duración, frecuencia, distribución por piloto y circuito) |

### Capturas de pantalla

<table>
  <tr>
    <td align="center"><img src="powerbi/1) Portada.jpg" width="420"/><br/><sub>Portada</sub></td>
    <td align="center"><img src="powerbi/2) Indice.jpg" width="420"/><br/><sub>Índice</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="powerbi/3) Glosario.jpg" width="420"/><br/><sub>Glosario</sub></td>
    <td align="center"><img src="powerbi/4) General.jpg" width="420"/><br/><sub>General</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="powerbi/5) Salida desde Pole.jpg" width="420"/><br/><sub>Salida desde Pole</sub></td>
    <td align="center"><img src="powerbi/6) Pilotos & Escuderías.jpg" width="420"/><br/><sub>Pilotos & Escuderías</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="powerbi/7) Evolución de Abandonos.jpg" width="420"/><br/><sub>Evolución de Abandonos</sub></td>
    <td align="center"><img src="powerbi/8) Pit Stops.jpg" width="420"/><br/><sub>Pit Stops</sub></td>
  </tr>
</table>

---

## 🛠️ Tecnologías

| Herramienta | Uso |
|-------------|-----|
| ![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black) | Visualización e interactividad del dashboard |
| ![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat&logo=powerbi&logoColor=black) | Medidas calculadas y KPIs |
| **Modelo Relacional** | Integración y estructura de las 14 tablas |
| ![MIRO](https://img.shields.io/badge/MIRO-FFD02F?style=flat&logo=miro&logoColor=050038) | Diseño del Diagrama Entidad-Relación |
| ![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white) | Fuentes de datos originales |

---

## 🗂️ Estructura del Proyecto

```
Formula1/
├── 📁 data/
│   ├── Base de Datos Integrada.xlsx   # Dataset completo (14 tablas, +20.000 registros)
│   └── README.md
├── 📁 powerbi/
│   ├── 1) Portada.jpg
│   ├── 2) Indice.jpg
│   ├── 3) Glosario.jpg
│   ├── 4) General.jpg
│   ├── 5) Salida desde Pole.jpg
│   ├── 6) Pilotos & Escuderías.jpg
│   ├── 7) Evolución de Abandonos.jpg
│   ├── 8) Pit Stops.jpg
│   └── README.md
├── 📁 report/
│   └── Informe de Análisis Fórmula 1.pdf
└── README.md
```

---

## 🚀 Futuras Líneas

- [ ] 📅 Incorporar datos de pit stops previos a 2011 para análisis histórico completo
- [ ] 🌦️ Agregar variables meteorológicas (lluvia, temperatura) como contexto de carrera
- [ ] 🗺️ Crear página de análisis dedicado por circuito
- [ ] ⚔️ Implementar comparación directa dinámica entre pilotos o escuderías

---

<div align="center">
  <sub>Proyecto desarrollado por <strong>Galosi Matias Gabriel</strong> — CoderHouse Data Analytics 2025</sub>
</div>
