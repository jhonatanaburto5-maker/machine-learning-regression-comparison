# 📊 Machine Learning Regression Model Comparison
![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green)

---

## 📌 Descripción

Este proyecto desarrolla un flujo completo de análisis de datos y Machine Learning para comparar el rendimiento de diferentes algoritmos de regresión utilizando Python.

Los modelos implementados fueron:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Elastic Net Regression

Cada modelo fue entrenado y evaluado utilizando diferentes métricas para determinar cuál ofrecía el mejor desempeño predictivo.

---

## 🎯 Objetivo

Comparar el rendimiento de distintos modelos de regresión mediante métricas estadísticas para identificar el algoritmo con mejor capacidad predictiva y generalización.

---
## 🗂 Dataset

- Número de registros: 36540
- Número de variables: 10 
- Variable objetivo: CO_2 Emisision
- Tipo de problema:  Predicción

---

## 🛠 Tecnologías

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Jupyter Notebook

---

## ⚙ Flujo de trabajo

✔ Importación de datos

✔ Limpieza de datos

✔ Análisis Exploratorio (EDA)

✔ División Train/Test

✔ Entrenamiento

✔ Evaluación

✔ Comparación de Modelos

✔ Interpretación de Resultados

---

## Comparación de modelos de regresión

Se evaluaron tres modelos de regresión utilizando las métricas **R²**, **RMSE** y **MAE**.  
Además, para los modelos regularizados (**Lasso** y **Ridge**) se incluye el valor óptimo del hiperparámetro de regularización (**alpha**) obtenido durante el ajuste.

| Modelo | R² | RMSE | MAE | Alpha | N° variables |
|:---|---:|---:|---:|---:|---:|
| Lasso | 0.0518 | 227.53 | 191.38 | 0.0464 | 57 |
| Ridge | 0.0509 | 227.63 | 191.49 | 166.81 | 119 |
| Regresión Lineal | 0.0329 | 229.78 | 193.15 | - | 7 |

### Interpretación de resultados

El modelo **Lasso Regression** obtuvo el mejor desempeño general, alcanzando el mayor valor de **R² (0.0518)** y los menores errores de predicción (**RMSE = 227.53** y **MAE = 191.38**).

Aunque la mejora respecto a los demás modelos es pequeña, Lasso logró reducir el número de variables utilizadas mediante la penalización L1, conservando únicamente **57 variables relevantes**.  

Por otro lado, **Ridge Regression** presentó un rendimiento similar, con un **R² de 0.0509**, pero manteniendo un mayor número de variables (**119**), debido a que la regularización L2 reduce la magnitud de los coeficientes sin eliminarlos completamente.

La **regresión lineal múltiple** obtuvo el menor desempeño, indicando que la incorporación de regularización y selección de variables aporta una ligera mejora al modelo predictivo.



