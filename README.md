#  [Producto3 Dataset de Mhealth]


## Abrir en Google Colab

Puedes ejecutar este notebook de forma interactiva en Google Colab sin necesidad de instalar nada en tu máquina local. Simplemente haz clic en el siguiente botón:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Jvviers/Proyecto_MHealth/blob/main/notebooks/Producto3_MHealth_Modelos_Gamboa.ipynb)

Proyecto de Reconocimiento de Actividades Humanas (HAR) usando el dataset MHEALTH. Compara el desempeño de Random Forest vs. Redes Neuronales (MLP).

##  Descripción del Proyecto

Este repositorio contiene el análisis y modelamiento predictivo del dataset MHEALTH como parte del Producto Computacional 3. El objetivo es construir un modelo capaz de clasificar 12 actividades humanas (L1-L12) basándose en 23 variables de sensores (acelerómetros, giroscopios, ECG).

### Metodología

1.  **Carga de Datos:** Se cargan y concatenan los 10 archivos `.log` del dataset, añadiendo un identificador de sujeto.
2.  **Preprocesamiento:** Se realiza una limpieza de datos, eliminando la "clase nula" (etiqueta 0). Los *features* son estandarizados usando `StandardScaler`.
3.  **Modelamiento:** Se implementan y comparan dos modelos:
    * **Machine Learning:** `RandomForestClassifier`
    * **Deep Learning:** `MLPClassifier` (Red Neuronal Densa)
4.  **Validación:** Los modelos se evalúan usando un split 70% entrenamiento / 30% prueba, con estratificación para mantener el balance de clases.

### Resultados Clave

El análisis concluye que el **Random Forest** es el modelo superior, alcanzando un **Accuracy del 99.18%**. Las curvas de aprendizaje y matrices de confusión demuestran que no solo es más preciso que el MLP (96.32%), sino que también generaliza mejor a datos nuevos sin sufrir de sobreajuste.