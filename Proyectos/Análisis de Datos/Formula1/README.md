# 🏎️ Fórmula 1 Historical Analysis (1950–2024)

Dashboard interactivo desarrollado en **Power BI** para analizar más de 70 años de historia de la Fórmula 1, desde la temporada inaugural en 1950 hasta 2024.

El proyecto explora tendencias históricas relacionadas con:

- 🏁 Rendimiento de Pilotos y Escuderías
- 🚦 Impacto de la posición de largada
- 🔧 Evolución de los Abandonos Mecánicos
- ⏱️ Estrategias y Tiempos de pit stop

---

## 🎯 Objetivo

Construir un dashboard interactivo que permita explorar métricas históricas de Fórmula 1 y validar hipótesis relacionadas con rendimiento, confiabilidad y estrategia.

---

## 📂 Dataset

El modelo integra información histórica de:

- carreras
- circuitos
- pilotos
- escuderías
- clasificaciones
- resultados
- pit stops
- tiempos de vuelta
- temporadas
- estados de carrera

📊 Más de 70 años de información histórica integrados en un modelo relacional de 14 tablas.

---

## 📌 Hallazgos principales

- Los pilotos que largan desde la pole position presentan una probabilidad de victoria significativamente superior al promedio histórico.
- La cantidad de abandonos por carrera disminuyó sostenidamente con el avance tecnológico de las últimas décadas.
- Ferrari, Mercedes y Red Bull dominaron gran parte de los campeonatos modernos.
- Los tiempos promedio de pit stop se redujeron drásticamente en la era moderna de la Fórmula 1.

---

## 📊 Dashboard

El dashboard incluye distintas páginas orientadas al análisis histórico y exploratorio:

| Página | Descripción |
|---|---|
| 🖼️ Portada | Presentación general del proyecto |
| 📑 Índice & Glosario | Navegación y conceptos utilizados |
| 📈 General | KPIs globales del campeonato |
| 🚦 Salida desde Pole | Impacto de la posición de largada |
| 🏅 Pilotos & Escuderías | Rankings y evolución histórica |
| 📉 Evolución de Abandonos | Tendencia histórica de retiros |
| 🔧 Pit Stops | Análisis de estrategias y tiempos en boxes |

---

## 🖼️ Capturas de pantalla

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

## 🛠️ Stack

| Área | Herramientas |
|---|---|
| Visualización | ![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black) |
| Modelado y métricas | ![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat&logo=powerbi&logoColor=black) |
| Diseño del modelo | Modelo relacional de 14 tablas |
| Diagramación | ![MIRO](https://img.shields.io/badge/MIRO-FFD02F?style=flat&logo=miro&logoColor=050038) |
| Fuente de datos | ![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white) |

---

## 📐 Métricas y medidas desarrolladas

Entre las principales métricas calculadas se incluyen:

- porcentaje de victorias desde pole position
- total y promedio de abandonos
- cantidad de podios y victorias
- vueltas rápidas por circuito
- ranking histórico de pilotos y escuderías
- victorias según posición de largada

---

## 🗂️ Estructura del proyecto

```bash
Formula1/
├── 📁 data/
│   ├── Base de Datos Integrada.xlsx
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

