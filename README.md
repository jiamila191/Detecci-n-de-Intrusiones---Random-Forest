#Detección de Intrusiones en Redes con Machine Learning

## Descripción del proyecto

Este proyecto implementa un Sistema de Detección de Intrusiones en Redes (NIDS) utilizando técnicas de Machine Learning, con el objetivo de clasificar el tráfico de red como normal (0) o malicioso (1).

Se trabaja con el dataset UNSW-NB15, ampliamente utilizado en investigaciones de ciberseguridad, y se desarrollan modelos basados en Random Forest y XGBoost, priorizando la detección de ataques y el análisis del comportamiento del tráfico.

El proyecto fue desarrollado como trabajo final en el marco de la formación como Analista de Datos Junior.

## Objetivos

Analizar y comprender el tráfico de red y sus características.

Detectar patrones de comportamiento malicioso mediante Machine Learning.

Desarrollar y evaluar un modelo de Random Forest para detección de intrusiones.

Comparar el rendimiento con otro modelo (XGBoost).

Evaluar métricas clave priorizando la seguridad (recall en ataques).

## Dataset

Nombre: UNSW-NB15

Origen: Australian Centre for Cyber Security (UNSW)

Características:

49 atributos de tráfico de red

Variables numéricas y categóricas

Múltiples tipos de ataques (DoS, Exploits, Reconnaissance, Worms, entre otros)

El dataset combina tráfico realista normal y malicioso, representando escenarios actuales de ciberseguridad.

## Metodología

Carga y exploración del dataset

Análisis exploratorio de datos (EDA)

Tratamiento de outliers y valores inconsistentes

Eliminación de variables altamente correlacionadas

Preprocesamiento con ColumnTransformer

Entrenamiento de modelos con Pipeline

Validación cruzada estratificada

Evaluación y comparación de modelos

## Modelos implementados
🔹 Random Forest

Ajuste de hiperparámetros

Priorización de la detección de ataques mediante class_weight

Excelente desempeño en recall para tráfico malicioso

🔹 Random Forest + SMOTE

Evaluación del balanceo de clases

No se observaron mejoras significativas debido al leve desbalance del dataset

🔹 XGBoost

Modelo de boosting para comparación

Buen rendimiento general, ligeramente inferior a Random Forest

## Resultados destacados

Random Forest:

Recall en ataques: 99%

Accuracy aproximada: 93%

AUC-ROC: 0.982

El modelo Random Forest demostró ser la mejor opción cuando se prioriza la seguridad, aceptando un mayor número de falsas alarmas.

## Tecnologías utilizadas

Python

Pandas, NumPy

Scikit-learn

Imbalanced-learn (SMOTE)

XGBoost

Matplotlib, Seaborn

Google Colab
