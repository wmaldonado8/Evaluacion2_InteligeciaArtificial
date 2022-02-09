# Evaluación 2 Inteligencia Artificial
**Integrantes:** 
- Santiago Tuqueres
- Cristian Medina
- Walter Maldonado
- Gabriel Viteri 

Dataset: Age and Body Performance(Edad y Rendimiento Corporal)

URL: [Body performance Data | Kaggle](https://www.kaggle.com/kukuroo3/body-performance-data)

## 1.  Análisis de Dataset
El Dataset elegido para el presente trabajo tiene como nombre “Age and Body Performance” obtenido en [1](#1), el cual tiene como objeto de estudio la edad y rendimiento corporal con el fin de observar características corporales y su relación con el rendimiento físico.
En dicho dataset destacan algunas columnas de datos, que tienen relación con características físicas del cuerpo detalladas a continuación:
-   Edad: se toma en cuenta las edades entre 20 a 64 años
-   Género: los géneros son femenino y masculino representados por F y M respectivamente. 
-   Altura: altura en centímetros.
-   Peso: peso de kilogramos.
-   Grasa Corporal: porcentaje de grasa corporal.
-   Presión Diastólica: presión de la sangre en la arteria cuando el corazón se relaja entre latidos; medido en minutos.
-   Presión Sistólica: presión de la sangre en la arteria cuando se contrae el corazón; media en minutos.

Seguidamente se busca entender la relación de dichas características físicas con el rendimiento en actividades físicas:
-   Fuerza de Agarre: es la fuerza utilizada con la mano para apretar o suspender objetos en el aire.
-   sentarse e inclinarse hacia adelante: es un estiramiento intenso para toda la parte posterior del cuerpo, desde los talones hasta la corona de la cabeza; medida en centímetros.
-   Abdominales: es una actividad física que se realiza con el objetivo de tonificar los músculos de la zona abdominal.
-   Salto de Longitud: salto de longitud que se realiza desde una posición de pie; medida en centímetros.

Con todas las variables mostradas anteriormente, el presente trabajo tiene como objetivo clasificar los datos y mostrar relaciones entre sus variables para entender como cambios en las características físicas pueden mejorar el rendimiento físico o viceversa que cambios en actividades físicas mejoran las características físicas.

## 2.  Elección de Algoritmo de Machine Learning
### Tabla de Algoritmos
|Algoritmo|Instancias correctamente clasificadas|
|---:|:---:|
|___Tipo___|___Trees___|
|Random Forest|74.5389 %|
|J48|68.6403 %|
|Decision Stump|41.0065 %|
|Hoeffding Tree|52.5797 %|
|LMT|71.4776 %|
|Random Tree|61.7636 %|
|REP Tree|68.4238 %|
|___Tipo___|___Rules___|
|ZeroR|24.9981 %|
|Decision Table|62.8836 %|
|JRip|63.4137 %|
|PART|68.8046 %|
|___Tipo___|___Bayes___|
|Bayes Net|56.6117 %|
|Naive Bayes|54.536  %|
|Naive Bayes Multinominal Text|24.9981 %|
|Naive Bayes Updateable|54.536  %|
|___Tipo___|___Meta___|
|Ada Bost M1|41.0065 %|
|Attribute Selected Classifer|56.4623 %|
|Bagging|72.3736 %|
|Classification Via Regression|72.3811 %|
|CVParameter Selection|24.9981 %|
|Fitered Classifier|64.4142 %|
|Iterative Classifier Optimizer|59.6879 %|
|Logit Boost|59.6879 %|
|Multi Class Classifier|59.3444 %|
|Multi Class Classifier Updateable|53.1696 %|
|Multi Scheme|24.9981 %|
|Random Commitee|71.7912 %|
|Randomizable Filtered Classifier|48.7344 %|
|Random Sub Space|68.9763 %|
|Stacking|24.9981 %|
|Vote|24.9981 %|
|Weightedlnstances Handler Wrapper|24.9981 %|

## 3.  Bibliografía
[1] <a name="1">“Edad y Rendimiento Corporal - ML | Kaggle.” https://www.kaggle.com/edenniss/age-and-body-performance-ml/notebook (accessed Feb. 06, 2022).</a>
