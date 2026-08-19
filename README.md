# 📊 Machine Learning Regression Model Comparison

![Python](https://img.shields.io/badge/Python-3.12%2B-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Machine%20Learning-F7931E?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

## 📌 Descripción

Este proyecto desarrolla un flujo de análisis de datos y Machine Learning para comparar diferentes modelos de regresión aplicados a la predicción de emisiones de CO₂ a partir de variables relacionadas con clima y energía.

Los modelos evaluados son:

- Regresión lineal múltiple
- Ridge Regression
- Lasso Regression
- Elastic Net Regression

El objetivo es comparar su desempeño mediante diferentes métricas y analizar cuál presenta el mejor comportamiento predictivo dentro del conjunto de datos utilizado.

## 🎯 Objetivo

Comparar el rendimiento de diferentes modelos de regresión para identificar cuál presenta el mejor desempeño predictivo, considerando tanto las métricas de error como la complejidad del modelo.

## 🗂 Dataset

- **Número de registros:** 36,540
- **Número de variables originales:** 10
- **Variable objetivo:** Emisiones de CO₂
- **Tipo de problema:** Regresión supervisada
- **Dominio:** Clima y energía

El dataset original no se incluye directamente en el repositorio. Para reproducir el análisis, consulta las indicaciones de la carpeta `data/`.

## 🛠 Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## ⚙️ Flujo de trabajo

1. Importación de los datos
2. Limpieza y revisión inicial
3. Validación de tipos de datos
4. Cambio y estandarización de nombres de columnas
5. Conversión de la variable de fecha
6. Análisis exploratorio de datos (EDA)
7. Análisis de correlación
8. División de los datos en entrenamiento y prueba
9. Estandarización de variables
10. Entrenamiento de los modelos
11. Validación cruzada
12. Ajuste de hiperparámetros para los modelos regularizados
13. Evaluación mediante R², RMSE, MAE y error máximo
14. Comparación e interpretación de resultados

## 📊 Comparación de modelos

| Modelo | R² | RMSE | MAE | Alpha | N.º de variables |
|:---|---:|---:|---:|---:|---:|
| **Lasso** | **0.0518** | **227.53** | **191.38** | 0.0464 | 57 |
| Ridge | 0.0509 | 227.63 | 191.49 | 166.81 | 119 |
| Regresión lineal | 0.0329 | 229.78 | 193.15 | — | 7 |

### Interpretación de resultados

El modelo **Lasso Regression** obtuvo el mejor desempeño general entre los modelos evaluados, alcanzando el mayor valor de **R² (0.0518)** y los menores valores de **RMSE (227.53)** y **MAE (191.38)**.

Aunque la diferencia respecto a Ridge es pequeña, Lasso utiliza regularización L1, lo que permite reducir algunos coeficientes hasta cero y obtener un modelo con menos variables.

Por otro lado, **Ridge Regression** presentó un rendimiento muy similar, con un **R² de 0.0509**. Debido a la regularización L2, sus coeficientes se reducen, pero no se eliminan completamente, por lo que mantiene un mayor número de variables.

La **regresión lineal múltiple** presentó el menor desempeño de los modelos comparados, con un **R² de 0.0329**.

### Consideración importante

A pesar de que Lasso obtuvo el mejor resultado, el **R² general es bajo**. Esto indica que las variables utilizadas en el modelo explican solamente una pequeña parte de la variabilidad observada en las emisiones de CO₂.

Por lo tanto, los resultados deben interpretarse como parte de un **estudio de modelado y comparación de algoritmos**, y no como evidencia de un sistema predictivo altamente preciso.

## 📁 Estructura del proyecto

```text
machine-learning-regression-comparison/
├── data/
│   └── README.md
├── Comparacion_modelo_regresion_lineal.ipynb
├── Energia.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## 🚀 Instalación

Clona el repositorio y crea un entorno virtual:

```bash
git clone https://github.com/jhonatanaburto5-maker/machine-learning-regression-comparison.git
cd machine-learning-regression-comparison
python -m venv .venv
```

En Windows:

```bash
.venv\Scripts\activate
```

Instala las dependencias:

```bash
pip install -r requirements.txt
```

Después, abre el notebook con Jupyter y configura la ruta del dataset según tu entorno local.

## 🔬 Reproducibilidad

El análisis utiliza una semilla fija (`random_state`) para la división de los datos y validación cruzada. Los modelos regularizados utilizan ajuste de hiperparámetros mediante `GridSearchCV` y la comparación se realiza utilizando métricas de error y capacidad explicativa.

## ⚠️ Limitaciones y próximos pasos

- El desempeño de los modelos lineales es limitado para el conjunto de datos utilizado.
- Se podría incorporar mayor información temporal y características específicas de cada país.
- Se podrían evaluar modelos no lineales, como Random Forest, Gradient Boosting y XGBoost.
- Se puede profundizar en el análisis de residuos y en la interpretación de los coeficientes.
- Sería conveniente realizar una validación externa antes de utilizar el modelo para decisiones operativas.

## 👤 Autor

**Jhonatan Aburto**  
Data Science & Energy Engineering

---

*Proyecto educativo y de portafolio orientado a la aplicación de Machine Learning sobre datos de clima y energía.*
