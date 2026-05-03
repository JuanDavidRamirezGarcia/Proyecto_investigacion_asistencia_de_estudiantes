# Predicción y análisis de asistencia de estudiantes en un proyecto educativo mediante técnicas de Machine Learning de un grupo de instituciones educativas de la ciudad de Medellín

## Descripción del Proyecto
Este proyecto busca resolver un problema crítico en la gestión de programas educativos: la incertidumbre sobre la asistencia estudiantil. Utilizando datos escolares, demográficos y de asistencia de estudiantes, a los talleres experienciales realizados en instituciones educativas, se desarrollaron modelos de Machine Learning para predecir si un estudiante asistirá o no a una sesión futura.

##  Problema y Contexto

Bajo el marco del programa Inspiración Comfama y la Fundación Loyola, se implementó un proyecto educativo en Medellín que integró talleres de modelado de materiales, nuevas tecnologías y desarrollo de software para estudiantes de sexto a undécimo grado. Con el fin de mejorar el impacto y la gestión de recursos de dicha intervención, surgió esta investigación independiente que utiliza los datos recolectados para analizar y predecir los patrones de asistencia estudiantil. El estudio emplea la asistencia de esta experiencia como base para un modelado predictivo autónomo, estableciendo el marco necesario para profundizar en el comportamiento de los participantes y fortalecer futuras ejecuciones educativas.

La asistencia es un elemento clave dentro de los proyectos educativos porque a partir de ella se evidencia el impacto de estos en la comunidad educativa en procesos de pertinencia y calidad de las enseñanzas impartidas. Según Barreno-Freine, Haro-Jácome y Florés-Yandún (2018), para garantizar un aprendizaje óptimo, la asistencia es fundamental porque tiene como objetivo el desarrollo de aprendizajes significativos de manera continua. A partir de aquí, lo oportuno es analizar y aplicar métodos de Machine Learning para identificar patrones de asistencia y deserción, fortaleciendo la planeación y el impacto de nuevas experiencias.

Dentro del proyecto educativo realizado no se encontraron causas puntuales de inasistencia, pero como se mencionó anteriormente, se vuelve importante analizar este tema. Sin embargo, no existen dentro del proyecto las herramientas que permitan analizar y predecir los datos de asistencia y actuar de forma preventiva. De no hacerlo, se podría afectar: la continuidad de los estudiantes, el aprovechamiento de recursos y la cobertura estudiantil.

Considerando la situación, se ve necesario realizar un análisis de datos y diseño de métodos de aprendizaje automático para identificar patrones de asistencia e inasistencia que puedan afectar la continuidad de los estudiantes.

Pregunta de investigación:¿La aplicación de modelos de machine learning a este proyecto educativo son una buena herramienta para encontrar patrones de asistencia?

##  Metodología y Gobernanza de Datos

El proyecto se realizó bajo una metodología **CRISP-DM**, a través de los siguientes pasos:

1. Comprensión del problema: La investigación fue de tipo cuantitativo ya que se analizaron datos numéricos y categóricos para calcular promedios, identificar tendencias y relaciones, y realizar predicciones en los datos estudiados. El proyecto se implementó bajo un diseño no experimental, observacional y longitudinal, ya que se analizaron datos de variables educativas y de asistencia sin manipularlas o transformarlas a lo largo de cuatro encuentros.

2. Población y muestra: La población fue el total de estudiantes de sexto a once de las tres instituciones educativas participantes en el programa. Y la muestra fueron los estudiantes que participaron en al menos una de las sesiones de los talleres del programa. 

3. Recolección y limpieza: Los datos recolectados son los datos de asistencia durante los cuatro encuentros del programa, los cuales incluyen variables como fecha de nacimiento, fecha del encuentro, género, tipo de taller, fecha de nacimiento y asistencia. Estos datos tuvieron un proceso de limpieza como depuración de datos inconsistentes, datos nulos y repetidos. Asimismo, como el cálculo de nuevas variables, como edad, promedio de asistencia previa y es de grado 9 o superior.

4. Análisis exploratorio de datos: En esta parte se realizó un análisis exploratorio de los datos para encontrar patrones y tendencias de asistencia, identificar valores atípicos y generar más preguntas e hipótesis.

5. Aplicación de los modelos de Machine Learning: Una vez se encontraron las variables más importantes para la asistencia, se entrenarón modelos de machine learning, como regresión logística y  árboles de decisión  para predecir la asistencia de estudiantes.

6. Evaluación del modelo: Se analizaron los resultados de los modelos para verificar qué tan efectivos y precisos fueron los modelos de machine learning mediante técnicas de desempeño como precisión, recall o F1-score.  


##  Resultados Clave

El desempeño de los modelos arrojó las siguientes métricas, destacando la Regresión Logística como la opción más equilibrada:

| Métrica | Árbol de Decisión | Random Forest | Regresión Logística |
| :--- | :---: | :---: | :---: |
| **Exactitud-Accuracy** | 77% | 77% | **79%** |
| **F1-Score (SI Asiste)** | 85% | 85% | **87%** |
| **F1-Score (NO Asiste)** | **52%** | **52%** | 51% |

### Conclusiones del Análisis
* La inasistencia fue el reto; los modelos alcanzaron un F1-Score de 52% para "No", evidenciando el efecto del desbalance de clases.
* Variables como la edad y la asistencia previa fueron buenos predictores de la asistencia.
* Los modelos actuales establecen una línea base para futuras investigaciones. Para que sean aplicables en programas reales, se requieren datos más balanceados o técnicas más avanzadas que mejoren la detección de inasistencias.



##  Estructura del Repositorio

```text
├── data/               # Muestra de la estructura de datos (anonimizada)
├── notebooks/          # Jupyter Notebooks con el EDA, limpieza y modelos
├── docs/               # Documentación del proyecto
│   ├── informe.pdf     # Propuesta y reporte de investigación completo
│   └── poster.pdf     # Presentación de resultados           
└── README.md           # Información del proyecto
```

## Tecnologías Utilizadas

* Lenguaje: Python
* Entorno de Desarrollo: Google Colab

Librerías Principales:
* pandas y numpy: Manipulación de datos.
* scikit-learn: Entrenamiento de modelos y métricas de evaluación.
* Matplotlib y seaborn: Visualización de datos.

# Trabajo a seguir

* Paso 1: enriquecer el modelo. Incorporar nuevas variables: personales, contextuales, de motivación para mejorar la predicción de la inasistencia.
* Paso 2: aplicar los modelos en proyectos futuros como herramientas de seguimiento.
* Paso 3: diseñar estrategias de retención para las últimas sesiones, donde la asistencia tiende a bajar.
* Paso 4: Diseñar un manual metodológico para que este modelo se pueda aplicar en otros colegios o proyectos educativos.


  # Quién realiza

 * Autor: Juan David Ramírez García
 * Email: david.ramirez@est.iudigital.edu.co
 * Universidad:  Semillero de Investigación en Desarrollo de Software - IUdigital de Antioquia

