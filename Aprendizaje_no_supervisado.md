# Análisis de Agrupamiento 

## Descripción General
Este proyecto implementa técnicas de aprendizaje no supervisado con el objetivo de identificar patrones y segmentar observaciones dentro de un conjunto de datos utilizando el algoritmo de clustering K-means. Se aplicaron diferentes enfoques de preprocesamiento y reducción de dimensionalidad para evaluar el impacto en la calidad de los clústeres generados.


## Composición de la Base de Datos

La base de datos utilizada contiene variables cuantitativas relacionadas con diferentes características o atributos de observaciones. Estas variables fueron estandarizadas para asegurar que todas tuvieran la misma escala, requisito fundamental para que el algoritmo K-means funcione correctamente. Aunque no se especifica el dominio exacto de los datos (por ejemplo, clientes, productos, regiones), cada fila representa una unidad de análisis que se desea clasificar automáticamente en grupos homogéneos.

## Procedimiento
### Se realizaron los siguientes pasos metodológicos:

#### 1) Preprocesamiento:

 * Estandarización de variables utilizando escalamiento estándar (StandardScaler).

 * Visualización preliminar y verificación de valores faltantes.

#### 2) Entrenamiento del modelo K-means:

 * Aplicación del algoritmo de K-means para agrupar las observaciones.

 * Determinación del número óptimo de clústeres (K) utilizando el método del codo y la métrica del Silhouette Score.

#### 3) omparación de enfoques:
 * Se utilizaron tres estrategias diferentes para el agrupamiento:

 * Dataset original: entrenamiento con todos los datos estandarizados.

 * Reducción de dimensionalidad con PCA: proyección a 2 componentes principales para simplificar la representación de los datos.

#### 4) Selección de características: entrenamiento con un subconjunto de variables relevantes seleccionadas manual o automáticamente.

## Evaluación de resultados:

 * Se calculó el Silhouette Score para cada enfoque como métrica de calidad del clustering.

 * Se construyó una visualización comparativa mediante un gráfico de barras.

## Resultados y Conclusiones
 * El método basado en PCA con 2 componentes principales alcanzó el mayor Silhouette Score (0.6267), indicando una segmentación más clara y definida.

 * El dataset original tuvo un desempeño intermedio con un score de 0.5483.

 * El enfoque con características seleccionadas obtuvo el menor puntaje (0.4694), mostrando menor cohesión y separación entre los grupos.

Conclusión: La reducción de dimensionalidad mediante PCA no solo simplificó la estructura de los datos, sino que también mejoró significativamente la calidad del agrupamiento. Esto demuestra que la transformación adecuada de los datos puede tener un impacto positivo en los resultados de técnicas no supervisadas.