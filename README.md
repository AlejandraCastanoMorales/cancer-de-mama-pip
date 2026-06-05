# cancer-de-mama-pip

# Análisis Predictivo y Exploratorio de Cáncer de Mama

## Contexto Historico y Motivación 

El cáncer de mama ha sido una de las enfermedades oncológicas más estudiadas debido a su alta frecuencia e impacto en la salud pública. Actualmente, la Organización Mundial de la Salud lo describe como un cáncer que se origina en los conductos o lobulillos mamarios, y señala que las formas tempranas pueden detectarse antes de que se conviertan en enfermedad invasiva. La detección temprana es clave porque los tumores identificados en fases iniciales suelen tener mejores posibilidades de tratamiento.

Durante gran parte del siglo XX, el diagnóstico del cáncer de mama dependió principalmente de la exploración clínica, la biopsia y el desarrollo progresivo de técnicas de imagen. La mamografía se consolidó como una herramienta central de tamizaje, especialmente desde la segunda mitad del siglo XX. La American Cancer Society señala que el objetivo del tamizaje es encontrar el cáncer antes de que cause síntomas, y que los cánceres detectados mediante exámenes de detección suelen ser más pequeños y menos propensos a haberse extendido fuera de la mama.

En años recientes, la predicción computacional en cáncer de mama ha cobrado mayor importancia por su potencial para apoyar procesos de diagnóstico temprano, priorización clínica y reducción de errores. Sin embargo, estos modelos deben entenderse como herramientas complementarias: pueden ayudar a identificar patrones en los datos, pero no reemplazan la evaluación médica, histopatológica ni radiológica.

Es por esto que el presente proyecto tiene como propósito estudiar las características celulares asociadas a tumores mamarios, con el fin de establecer relaciones entre dichas variables y el tipo de diagnóstico presentado. A partir de la información contenida en la base de datos, se pretende identificar patrones que permitan distinguir entre tumores benignos y malignos, aportando una aproximación basada en datos que contribuya al análisis predictivo del cáncer de mama y al fortalecimiento de estrategias de apoyo al diagnóstico temprano.

## Descripción General del Proyecto

El presente proyecto computacional tiene como objetivo realizar un análisis exhaustivo y la preparación técnica de datos orientada a la predicción del cáncer de mama. Utilizando el **Breast Cancer Wisconsin (Diagnostic) Dataset**

Este repositorio documenta las fases iniciales y más críticas del modelado predictivo: el Análisis Exploratorio de Datos (EDA) y la ingeniería de características, garantizando que los datos introducidos a futuros modelos predictivos sean limpios, insesgados y estadísticamente estables.

---

## Estructura del Repositorio

* `main.py` / `main.ipynb`: Código fuente principal que contiene la lógica operativa del proyecto.
* `dataset.md`: Documentación técnica que detalla el origen, naturaleza y diccionario de variables del conjunto de datos.
* `workflow.md`: Representación gráfica (diagrama de flujo) de la arquitectura del código.
* `requirements.txt`: Lista de dependencias de la Biblioteca Estándar y de terceros necesarias para la ejecución.
* `cancer_de_mama.csv`: Archivo de datos de entrada (si aplica según las políticas de privacidad del repositorio).

---

## Tecnologías y Librerías Utilizadas

El proyecto está desarrollado en **Python 3** y hace uso de las siguientes librerías especializadas:
* **Pandas & NumPy:** Manipulación de estructuras de datos y cálculos numéricos.
* **Matplotlib & Seaborn:** Generación de gráficos y visualización estadística avanzada.
* **Scikit-learn:** Herramientas de preprocesamiento, escalamiento y división de datos para Machine Learning.

---

## Metodología y Fases del Código

El código principal está estructurado de manera secuencial. A continuación, se detalla qué se realizó en cada fase y el propósito técnico de cada paso:

### Fase 1: Ingesta de Datos
* **Acción:** Se utilizó la librería Pandas para leer el archivo local `.csv` y cargarlo en un DataFrame.
* **Propósito:** Transferir la información estática del archivo a la memoria de trabajo del entorno de Python para permitir su manipulación analítica.

### Fase 2: Análisis Exploratorio de Datos (EDA)
* **Acción:** Se ejecutaron funciones de inspección (como `info()`, `describe()`) y se verificó la existencia de valores nulos y registros duplicados.
* **Propósito:** Auditar la calidad del conjunto de datos. Un modelo de Machine Learning es tan bueno como los datos que lo alimentan; confirmar la ausencia de datos nulos garantiza que el modelo no sufra fallos matemáticos durante su entrenamiento.

### Fase 3: Análisis Visual Estadístico
* **Acción:** Se generaron histogramas, diagramas de caja (boxplots), mapas de calor (heatmaps) de correlación y gráficos de dispersión múltiple (pairplots).
* **Propósito:** * **Univariado:** Identificar la distribución de cada variable individual y detectar valores atípicos (outliers) que pudieran sesgar el modelo.
  * **Bivariado:** Entender la relación matemática (correlación de Pearson) entre las características celulares y el diagnóstico. Esto permite identificar qué variables tienen el mayor poder predictivo.

### Fase 4: Preparación para Machine Learning
* **Acción:** Separación de variables predictoras (`X`) y variable objetivo (`y`), división del conjunto en datos de entrenamiento y prueba (Train/Test Split) y estandarización matemática (StandardScaler).
* **Propósito:**
  * **División (80% / 20%):** Se aísla un 20% de los datos para que el modelo nunca los vea durante el entrenamiento. Esto permite evaluar su precisión real en casos nuevos y evitar el sobreajuste (*overfitting*).
  * **Escalamiento:** Las variables originales tienen unidades de medida muy distintas (ej. áreas grandes frente a dimensiones fractales diminutas). El escalamiento ajusta todas las variables a una escala estándar (media de 0 y desviación estándar de 1) para que el algoritmo asigne el peso correcto a cada característica sin verse sesgado por magnitudes absolutas.

---

