# Predicción y análisis de asistencia de estudiantes en un proyecto educativo mediante técnicas de Machine Learning de un grupo de instituciones educativas de la ciudad de Medellín

## Descripción del Proyecto
Este proyecto busca resolver un problema crítico en la gestión de programas educativos: la incertidumbre sobre la asistencia estudiantil. Utilizando datos históricos de talleres experienciales realizados en colegios de Medellín, se desarrollaron modelos de Machine Learning para predecir si un estudiante asistirá o no a una sesión futura.

##  Problema y Contexto

Los programas educativos extracurriculares enfrentan el reto de la deserción y la inasistencia fluctuante. 
Sin herramientas predictivas, es difícil para los administradores:
* Planear los recursos eficientemente
* Identificar estudiantes en riesgo de abandono antes de que dejen de asistir.
* Entender qué factores (edad, grado, historial) influyen en la permanencia.

##  Metodología y Gobernanza de Datos

El proyecto siguió un diseño **longitudinal y observacional**, estructurado en las siguientes fases:

1.  **Recolección de datos:** datos de asistencia de 3 instituciones educativas (Grados 6° a 11°).
2.  **Limpieza y calidad de datos:** depuración de datos nulos, eliminación de duplicados y estandarización de formatos.
3.  **Ingeniería de datos:** creación de variables clave como: `asistencia_previa`, `promedio_asistencia`, `es_grado_superior`, `numero_sesion`.
4.  **Modelado y análisis exploratorio de datos** Se entrenaron y evaluaron tres algoritmos supervisados:
    * Regresión Logística (Logistic Regression).
    * Árboles de Decisión (Decision Tree).
    * Bosques Aleatorios (Random Forest).

##  Resultados Clave

El desempeño de los modelos arrojó las siguientes métricas, destacando la Regresión Logística como la opción más equilibrada:

| Modelo | Exactitud (Accuracy) | F1-Score (SÍ Asiste) | F1-Score (NO Asiste) | Diagnóstico |
| :--- | :---: | :---: | :---: | :--- |
| **Regresión Logística** | **79.7%** | **0.87** | 0.51 | **Mejor Modelo.** El más equilibrado y simple. |
| Árbol de Decisión | 77.0% | 0.85 | 0.52 | Alta precisión en asistencia, baja en inasistencia. |
| Random Forest | 77.0% | 0.85 | 0.52 | Sin mejora significativa respecto al árbol simple. |

### Conclusiones del Análisis
*  **Efectividad:** Los modelos son excelentes (**~91% de precisión**) para confirmar quiénes **SÍ** asistirán.
*  **La debilidad:** La predicción de la inasistencia (quién faltará) es compleja (Precisión ~43-47%), lo que sugiere que faltan variables cualitativas (motivación, problemas familiares) en los datos actuales.
*  **Patrón:** La asistencia previa es el predictor más fuerte del comportamiento futuro.

##  Estructura del Repositorio

```text
├── data/               # Muestra de la estructura de datos (anonimizada)
├── notebooks/          # Jupyter Notebooks con el EDA, limpieza y modelos
├── docs/               # Documentación del proyecto
│   ├── informe.pdf     # Propuesta y reporte de investigación completo
│   └── slides.pdf      # Presentación ejecutiva de resultados
├── images/             # Gráficos generados y visualizaciones del EDA
└── README.md           # Información del proyecto
```

## Tecnologías Utilizadas

* Lenguaje: Python
* Entorno de Desarrollo: Google Colab

Librerías Principales:
* pandas y numpy: Manipulación de datos.
* scikit-learn: Entrenamiento de modelos y métricas de evaluación.
* matplotlib y seaborn: Visualización de datos.

# Trabajo Futuro

* Enriquecer Datos: Incorporar variables cualitativas (encuestas de satisfacción, entorno familiar).
* Intervención: Diseñar un sistema de alertas tempranas para estudiantes con alta probabilidad de inasistencia ("Riesgo Detectado").
* Despliegue: Empaquetar el modelo en una aplicación web sencilla para uso de los coordinadores académicos.

  # Quién realiza

 * Autor: Juan David Ramírez García
 * Email: david.ramirez@est.iudigital.edu.co
 * Universidad:  Semillero de Investigación en Desarrollo de Software - IUdigital de Antioquia

