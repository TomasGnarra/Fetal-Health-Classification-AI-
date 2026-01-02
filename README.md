#  Fetal-Health-Classification-AI-Predicción de Salud Fetal con IA (Cardiotocografía)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Medical Data](https://img.shields.io/badge/HealthTech-Medical_Diagnosis-red?style=for-the-badge&logo=red-cross&logoColor=white)

> **Objetivo:** Desarrollar una herramienta de apoyo al diagnóstico médico para reducir la mortalidad perinatal mediante la clasificación automática de cardiotocogramas (CTG).

---

### 🏥 Contexto del Problema
Las complicaciones durante el parto son una causa mayor de mortalidad. El análisis manual de los CTG (frecuencia cardíaca fetal, movimientos, contracciones) es complejo y sujeto a la fatiga del especialista.

Este proyecto utiliza un dataset de **2.126 exámenes** clasificados por obstetras expertos para entrenar un modelo capaz de detectar automáticamente si el estado del feto es **Normal** o **Patológico** (Anormal).

---

### ⚙️ Metodología y Flujo de Trabajo

**1. Análisis Exploratorio (EDA):**
- Estudio de correlaciones entre movimientos fetales y variabilidad cardíaca.
- Detección de desbalance de clases (mayoría de casos normales vs. minoría patológicos).

**2. Preprocesamiento:**
- Limpieza de datos y manejo de valores nulos.
- División estratégica en conjuntos de **Entrenamiento y Test** para evitar el sobreajuste (overfitting).

**3. Modelado Predictivo:**
Se evaluaron y ajustaron los siguientes algoritmos para maximizar la detección de casos de riesgo (Recall):
- **Random Forest Classifier** (Seleccionado como el mejor modelo).
- Decision Trees.
- K-Nearest Neighbors (KNN).

---

### 📊 Resultados del Modelo (Performance)

El modelo final fue validado utilizando curvas ROC y matrices de confusión para asegurar que los "Falsos Negativos" (decir que un bebé está sano cuando no lo está) sean mínimos.

| Métrica | Resultado | Interpretación |
| :--- | :--- | :--- |
| **Accuracy** | **94%** | Precisión global del modelo. |
| **Recall** | **Alto** | Capacidad crítica para detectar fetos en riesgo. |
| **AUC-ROC** | **0.96** | Excelente capacidad de distinción entre clases. |

> *Nota: El modelo actúa como una "segunda opinión" digital para priorizar la atención médica en salas de parto congestionadas.*

---

### 🛠 Tech Stack
- **Lenguaje:** Python 3.9
- **Librerías:** Pandas, Numpy, Matplotlib, Seaborn (Visualización).
- **ML Core:** Scikit-Learn (Model Selection, Metrics).

---

### 📂 Estructura del Proyecto
- `/notebooks`: Código completo con el análisis paso a paso.
- `/data`: Dataset procesado de cardiotocogramas.
- `/reports`: Informe ejecutivo de resultados y curvas ROC.

---
*Autor: Tomas Gnarra*
