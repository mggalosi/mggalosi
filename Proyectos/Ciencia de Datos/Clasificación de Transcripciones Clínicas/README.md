# 🏥 Clasificación de transcripciones clínicas — NLP + Deep Learning


Proyecto de clasificación binaria de texto médico para determinar si una transcripción clínica corresponde a una especialidad quirúrgica (`Surgery = 1`) o no quirúrgica (`Surgery = 0`).

En Argentina los datos clínicos en texto libre no están disponibles públicamente por restricciones de privacidad. Se utilizó el dataset [Medical Transcriptions (Kaggle)](https://www.kaggle.com/datasets/tboyle10/medicaltranscriptions) como proxy para demostrar las técnicas aplicables al sistema de salud.

El proyecto explora:
- preprocesamiento de texto clínico con técnicas de NLP,
- comparativa de lematización entre NLTK y spaCy,
- representación vectorial con TF-IDF y BOW,
- entrenamiento de modelos baseline y una red neuronal en PyTorch,
- y análisis de limitaciones por desbalance de clases.

---

## 📦 Dataset

| Campo | Detalle |
|---|---|
| Fuente | Kaggle — tboyle10/medicaltranscriptions |
| Registros válidos | 4.966 (se eliminaron 33 filas con `transcription` nula) |
| Variable objetivo | `label` — Surgery (1) / No Surgery (0) |
| Desbalance de clases | ~78% No Surgery / ~22% Surgery |

---

## 📌 Análisis realizados

**Etapa 1 — NLP**
- Limpieza de texto con expresiones regulares (minúsculas, números, puntuación)
- Tokenización, remoción de stopwords y lematización con NLTK
- Comparativa de lematización: NLTK vs. spaCy
- Nubes de palabras por clase
- Análisis de bigramas y sentimiento con TextBlob

**Etapa 2 — Modelado**
- Representación vectorial: BOW (CountVectorizer) vs. TF-IDF
- Modelos baseline con Regresión Logística
- Red neuronal densa en PyTorch con Batch Normalization, Dropout(0.5) y Early Stopping
- Comparación de modelos: Accuracy, F1-Score Surgery y AUC-ROC

---

## 📊 Resultados

| Modelo | Accuracy | F1-Score Surgery | AUC-ROC |
|---|---|---|---|
| BOW + Regresión Logística | 0.64 | 0.19 | 0.71 |
| TF-IDF + Regresión Logística | 0.71 | 0.16 | 0.79 |
| **PyTorch TextClassifier** | **0.73** | **0.18** | **0.80** |

El desbalance de clases fue el principal limitante: ningún modelo superó un F1-Score de 0.19 para Surgery. En un contexto clínico real, el recall de la clase quirúrgica es la métrica más crítica — no detectar un caso quirúrgico tiene mayor costo que generar una falsa alarma.

---

## 🛠️ Stack técnico

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-154F5B?style=flat&logoColor=white)
![spaCy](https://img.shields.io/badge/spaCy-09A3D5?style=flat&logo=spacy&logoColor=white)
