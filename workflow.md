# Flujo de Trabajo: Análisis de Cáncer de Mama

Este documento describe paso a paso la lógica implementada en el código principal del proyecto, desde la carga de datos hasta la preparación para los modelos de Machine Learning.

## Diagrama de Flujo (Pipeline)

```mermaid
graph TD
    A([Inicio]) --> B[Importar Librerías<br>Numpy, Pandas, Sklearn, etc.]
    B --> C[(Cargar Dataset<br>cancer_de_mama.csv)]
    
    C --> D{Análisis Exploratorio EDA}
    D --> E[Inspección inicial<br>Forma, Tipos y Estadísticos]
    E --> F[Limpieza y Validación<br>Revisar Nulos y Duplicados]
    
    F --> G{Análisis Visual}
    G --> H[Análisis Univariado<br>Histogramas y Boxplots]
    H --> I[Análisis Bivariado<br>Mapa de calor y Pairplot]
    
    I --> J{Preparación para Machine Learning}
    J --> K["Separar Variables<br>X: Predictoras | y: Target"]
    K --> L[División Train/Test<br>80% Entrenamiento / 20% Prueba]
    L --> M[Escalamiento de Datos<br>StandardScaler]
    
    M --> N([Datos listos para el Modelo])
    
    %% Estilos del diagrama
    style A fill:#4CAF50,stroke:#fff,stroke-width:2px,color:#fff
    style N fill:#4CAF50,stroke:#fff,stroke-width:2px,color:#fff
    style C fill:#2196F3,stroke:#fff,stroke-width:2px,color:#fff
    style D fill:#FF9800,stroke:#fff,stroke-width:2px,color:#fff
    style G fill:#FF9800,stroke:#fff,stroke-width:2px,color:#fff
    style J fill:#FF9800,stroke:#fff,stroke-width:2px,color:#fff