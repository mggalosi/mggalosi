# ⛽ Análisis y Predicción de Precios de Combustibles en Argentina

Proyecto de ciencia de datos sobre la evolución de precios de combustibles en Argentina utilizando datos públicos oficiales.

El análisis explora:
- tendencias históricas,
- diferencias regionales,
- comportamiento por tipo de combustible,
- y modelos predictivos de precios.

📂 Dataset: datos.gob.ar — Resolución 314/2016

---

## 📊 Dataset

- 36.823 registros
- 3.494 empresas
- 1.066 localidades
- Período analizado: 2017–2024

---

## 📌 Principales hallazgos

### 🔄 Cambio estructural en 2022

El Gas Oil pasó de ser históricamente más barato que la Nafta a superar su precio promedio, mostrando una tendencia creciente estadísticamente significativa.

### 🗺️ Diferencias regionales

Se detectaron diferencias sistemáticas entre regiones:
- NEA y región Pampeana presentan precios consistentemente más altos.
- El comportamiento territorial se mantiene incluso controlando por outliers.

### 📈 Tendencia temporal

La Nafta presenta una tasa de crecimiento anual superior al Gas Oil.

---

## 🤖 Modelado predictivo

Se entrenaron distintos modelos de machine learning para estimar el precio por litro utilizando variables:
- temporales,
- geográficas,
- comerciales,
- y categóricas.

### 📊 Resultados

| Modelo | R² | MAPE |
|---|---|---|
| Random Forest | 0.98 | 2.8% |
| Gradient Boosting | 0.98 | 5.5% |
| Ridge Regression | 0.85 | ~67% |

### 🏆 Mejor modelo

Random Forest obtuvo el mejor desempeño, evidenciando relaciones no lineales entre:
- región,
- tiempo,
- empresa,
- y tipo de combustible.

---

## 📸 Visualizaciones

### 📈 Evolución temporal

<table>
  <tr>
    <td align="center">
      <img src="../images/01_evolucion_temporal_precio_anual.png" width="420"/>
      <br/>
    </td>
    <td align="center">
      <img src="../images/02_evolucion_temporal_por_region.png" width="1000"/>
      <br/>
    </td>
  </tr>
</table>

---

### 🗺️ Diferencias regionales

<table>
  <tr>
    <td align="center">
      <img src="../images/03_diferencias_regionales_precio_promedio.png" width="550"/>
      <br/>
    </td>
    <td align="center">
      <img src="../images/04_diferencias_regionales_cv.png" width="550"/>
      <br/>
    </td>
  </tr>
</table>

---

### 📊 Distribución de precios

<table>
  <tr>
    <td align="center">
      <img src="../images/05_distribucion_precios_boxplot_global.png" width="550"/>
      <br/>
    </td>
    <td align="center">
      <img src="../images/06_distribucion_precios_boxplot_por_producto.png" width="550"/>
      <br/>
    </td>
  </tr>
</table>

---

### 🌲 Importancia de variables

<table>
  <tr>
    <td align="center">
      <img src="../images/07_importancia_variables_correlacion_heatmap.png" width="550"/>
      <br/>
    </td>
    <td align="center">
      <img src="../images/08_importancia_variables_distribucion_features.png" width="650"/>
      <br/>
    </td>
  </tr>
</table>

---

### 🤖 Predicciones vs valores reales

<table>
  <tr>
    <td align="center">
      <img src="../images/09_predicciones_vs_reales_scatter.png" width="1000"/>
      <br/>
    </td>
    <td align="center">
      <img src="../images/10_predicciones_vs_reales_residuos.png" width="1000"/>
      <br/>
    </td>
  </tr>
</table>

---

## 🛠️ Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=matplotlib&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)