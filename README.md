# 🎓 Trabajo Final: Sistema de Scoring Crediticio con Deep Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-Redes_Neuronales-red?style=for-the-badge&logo=keras&logoColor=white)
![Status](https://img.shields.io/badge/Status-Finalizado-success?style=for-the-badge)

> **Diplomado en Data Science & Business Intelligence** > *Módulo:* Fundamentos de Redes Neuronales (R y Python)  
> **Docente:** Orbegoso Salas, Istavay Alberto

---

## 🏦 Caso de Negocio: Predicción de Riesgo en NOVA Card

### 📋 Resumen Ejecutivo
Este proyecto aborda el desafío crítico de la gestión de riesgo financiero mediante el desarrollo de una arquitectura de **Aprendizaje Profundo (Deep Learning)**. 

El objetivo principal fue orquestar un modelo predictivo capaz de identificar patrones complejos no lineales asociados al **incumplimiento de pago (Default)** y la **deserción de clientes (Churn)**, permitiendo a la entidad financiera optimizar su exposición al riesgo y personalizar sus estrategias de retención.

---

## 💡 Impacto Técnico y Metodológico

El valor diferencial de este proyecto radica en la implementación rigurosa de conceptos avanzados de redes neuronales y la **calibración neuronal** para garantizar la robustez del modelo en un entorno productivo:

### 1. Arquitectura y Retropropagación
Diseño de una red neuronal densa (*Feedforward*) optimizada mediante el algoritmo de **Retropropagación (Backpropagation)**, permitiendo el ajuste eficiente de los pesos sinápticos a través de múltiples capas ocultas para capturar abstracciones de alto nivel en los datos.

### 2. Optimización del Descenso de Gradiente
Implementación del optimizador **Adam**, una variante avanzada del **Descenso de Gradiente Estocástico**, ajustando la tasa de aprendizaje (*learning rate*) para acelerar la convergencia hacia el mínimo global de la función de coste.

### 3. Control de Varianza (Overfitting/Underfitting)
Para mitigar el **sobreajuste (Overfitting)** y garantizar que el modelo generalice correctamente ante nuevos datos, se desplegó una estrategia defensiva en capas:

* **Regularización L1 (Lasso) y L2 (Ridge):** Penalización de los pesos sinápticos para reducir la complejidad del modelo y seleccionar las características más relevantes.
* **Dropout (30%):** Desactivación aleatoria de neuronas durante el entrenamiento para forzar la redundancia y robustez de la red.
* **Early Stopping:** Monitorización constante de la métrica de pérdida en validación para detener el entrenamiento en el punto óptimo, evitando el deterioro por sobre-entrenamiento.

### 4. Ajuste de Hiperparámetros
*Tuning* exhaustivo de **Parámetros e Hiperparámetros** críticos (número de neuronas, *batch size*, épocas y funciones de activación ReLU/Sigmoide) para maximizar métricas de negocio como el AUC y Gini.

---

## 🛠️ Stack Tecnológico

| Categoría | Herramientas Utilizadas |
| :--- | :--- |
| **Lenguaje Core** | Python 3.x |
| **Deep Learning** | TensorFlow 2.x, Keras (Sequential API) |
| **Ingeniería de Datos** | Pandas, NumPy, Scikit-Learn (FactorAnalysis, StandardScaler) |
| **Visualización** | Seaborn, Matplotlib (Análisis de curvas de aprendizaje) |

---

## 🔍 Resultados Cuantitativos

El modelo final demostró una alta capacidad de discriminación, validada mediante métricas estándar de la industria bancaria:

1.  **Performance del Modelo:**
    * **Accuracy:** ~90.60% (Global)
    * **AUC Score (ROC):** `0.9183` (Excelente capacidad de discriminación).
    * **Índice de Gini:** `0.8366`
2.  **Segmentación Psicométrica:**
    * Aplicación de algoritmos no supervisados (**Factor Analysis**) para sintetizar variables latentes como *Autocontrol* e *Impulsividad*, enriqueciendo la capacidad predictiva del modelo supervisado.

---

## 👥 Equipo de Data Science

* **Estela Ramos, Christian Gean Pier**
* **Zuñe Cordova, Vivian Melissa**

---
