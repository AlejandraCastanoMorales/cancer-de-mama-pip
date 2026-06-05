# Documentación del Dataset: Breast Cancer Wisconsin (Diagnostic)

Este documento detalla la naturaleza, el origen y la estructura del conjunto de datos utilizado en este proyecto para la predicción y análisis del cáncer de mama.

---

## 1. Origen y Naturaleza de los Datos

* **Fuente oficial**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)) (También disponible en plataformas como Kaggle).
* **Naturaleza:** Es una base de datos **completamente pública** y de libre uso para fines de investigación y educación.
* **Creadores:** Dr. William H. Wolberg, W. Nick Street y Olvi L. Mangasarian (Universidad de Wisconsin, 1995).
* **Método de recolección:** Los datos fueron calculados a partir de imágenes digitalizadas de una biopsia mamaria (Aspiración con Aguja Fina - PAAF). Estas imágenes describen las características de los núcleos celulares presentes en la muestra.

---

## 2. Descripción General

El conjunto de datos consta de las siguientes dimensiones:
* **Filas (Instancias):** 569 pacientes/muestras.
* **Columnas (Variables):** 32 atributos en total (1 identificador único, 1 variable objetivo categórica y 30 variables numéricas).
* **Valores nulos:** El dataset original está completo, no contiene valores faltantes.

---

## 3. Diccionario de Datos (Variables)

### Variable Objetivo (Target)
Es la variable que nuestro modelo intentará predecir o explicar:
* `diagnosis`: El diagnóstico de la masa mamaria. Puede tomar dos valores:
  * **M** = Maligno (Cáncer presente).
  * **B** = Benigno (Cáncer ausente).



**Nota importante:** Para cada una de estas 10 características, el dataset incluye 3 medidas estadísticas distintas, lo que nos da el total de 30 variables numéricas:
* **Mean (Promedio):** El valor medio de esa característica (ej. `radius_mean`).
* **SE (Error Estándar):** El error estándar de esa característica (ej. `radius_se`).
* **Worst (Peor/Mayor):** El valor promedio de los 3 núcleos más grandes encontrados (ej. `radius_worst`).

---

