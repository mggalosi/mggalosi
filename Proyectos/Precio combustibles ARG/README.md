# ⛽ Análisis y Predicción de Precios de Combustibles en Argentina (2017–2026)

**Proyecto Final — Data Science 2: Machine Learning para la Ciencia de Datos**  
👤 Autor: Galosi | 🏫 Curso: CoderHouse

---

## 📋 Descripción

Análisis estructural de los precios de **Nafta Súper** y **Gas Oil Grado 2** en Argentina durante el período 2017–2026, combinando análisis exploratorio estadístico con modelos de Machine Learning para predecir el precio de venta por litro en función de variables temporales, geográficas y comerciales.

📂 **Dataset fuente:** [datos.gob.ar — Resolución 314/2016](https://datos.gob.ar/dataset/energia-precios-surtidor---resolucion-3142016)  
📊 **36.823 registros** · 🏢 **3.494 empresas** · 📍 **1.066 localidades**

---

## 🗂️ Estructura del Notebook

| # | Sección | Descripción |
|---|---------|-------------|
| 1 | 📖 Introducción | Abstract, fuente de datos y preguntas de investigación |
| 2–3 | ⚙️ Setup | Importación de librerías y carga del dataset |
| 4–5 | 🔍 Data Profiling & Quality | Validación, tratamiento de nulos y outliers (IQR por año y producto) |
| 6 | 🔧 Data Wrangling | Construcción de métricas agregadas, variable brecha y dataset territorial |
| 7 | 📊 EDA | Respuesta estadística a 5 preguntas de investigación (Levene, regresión con interacción, ANOVA) |
| 8–9 | 🛠️ Feature Engineering & Correlaciones | 8 variables predictoras con codificación cíclica del mes |
| 10–11 | 🤖 Modelado ML | Comparación de 4 modelos en dataset histórico y reciente |
| 12 | 📈 Análisis Comparativo | Tabla resumen, interpretación y conclusiones |
| 13–15 | 🧪 Diagnóstico Estadístico | Escalado (RobustScaler), validación cruzada, GridSearchCV, Shapiro-Wilk, curvas de aprendizaje |

---

## 💡 Principales Hallazgos

- 🔄 **Cambio estructural 2022:** el hallazgo más relevante. La brecha de precios invirtió su signo — el Gas Oil pasó de ser más barato a superar el precio de la Nafta — con una tendencia creciente estadísticamente significativa (β = 8,55 $/año, p = 0,0013).
- 🗺️ **Heterogeneidad territorial:** el test ANOVA confirma diferencias significativas entre regiones (p < 0,001). NEA y la región Pampeana presentan precios sistemáticamente superiores.
- 📈 **Tendencia temporal:** la Nafta crece a una tasa anual ~4% superior a la del Gas Oil (p < 0,001).
- 🛡️ **Robustez:** los resultados se mantienen al controlar por outliers, con excepción del año 2023 (impacto de ≈8–9% por alta volatilidad macroeconómica).

---

## 🏆 Resultados del Modelado

| Modelo | R² Histórico | R² Reciente | MAPE |
|--------|:------------:|:-----------:|:----:|
| 🥇 Random Forest | 0.9846 | 0.9511 | 2.8% |
| 🥈 Gradient Boosting | 0.9827 | 0.9473 | 5.5% |
| 🥉 Ridge / Reg. Lineal | 0.8491 | 0.8908 | ~67% |

> ✅ **Modelo recomendado: Random Forest.** La brecha de ~10 puntos de R² respecto a los modelos lineales evidencia relaciones predominantemente no lineales entre precio, región, empresa y tiempo. El MAPE < 4% en ambos datasets indica error relativo muy bajo incluso en un contexto inflacionario.

---

## 🛠️ Tecnologías

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=matplotlib&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)
