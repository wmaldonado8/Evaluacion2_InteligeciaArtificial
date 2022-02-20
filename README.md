# Evaluación 2 Inteligencia Artificial
**Integrantes:** 
- Santiago Tuqueres
- Cristian Medina
- Walter Maldonado
- Gabriel Viteri 

Dataset: Age and Body Performance(Edad y Rendimiento Corporal)

URL: [Body performance Data | Kaggle](https://www.kaggle.com/kukuroo3/body-performance-data)

## 1.  Análisis de Dataset
El Dataset elegido para el presente trabajo tiene como nombre “Age and Body Performance” obtenido en [1](#c1), el cual tiene como objeto de estudio la edad y rendimiento corporal con el fin de observar características corporales y su relación con el rendimiento físico.
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
### Tabla de prueba de algoritmos en dataset
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

<a name="t1">Tabla 1: Prueba de algoritmos con dataset<a>

Cuando se trabaja con un problema de aprendizaje automático, como en este caso, no se puede saber de antemano qué algoritmo será el mejor por ello: 

>La solución es probar un conjunto de algoritmos sobre su problema y ver qué funciona mejor esto le dará una idea del tipo general de algoritmos que funcionan bien o estrategias de aprendizaje que pueden ser mejores que el promedio para elegir la estructura oculta en sus datos [2](#c2).
>- J. Brownlee
  
De entre los algoritmos mencionados anteriormente podemos ver los tipo de algoritmos como[3](#c3):
  -   Regresion: en este método lo que se espera es un número, no lo ubica en un grupo, sino
      que devuelve un valor específico.
  -   Bayesianos: Este tipo de algoritmos por clasificación están basados en el teorema de Bayes y clasifican cada valor como independiente de cualquier otro. Lo       que permite predecir una clase o categoría en función de un conjunto dado de características, utilizando la probabilidad.
  -   Agrupacion: Se utilizan en el aprendizaje no supervisado, y sirven para categorizar datos no etiquetados, es decir, datos sin categorías o grupos definidos.
  -   Redes Neuronales: comprende unidades dispuestas en una serie de capas, cada una de las cuales se conecta a las capas anexas. Las RNA se inspiran en los           sistemas biológicos, como el cerebro, y en cómo procesan la información.
  -   Reduccion de Dimension: La reducción de dimensión reduce el número de variables que se consideran para encontrar la información exacta requerida.
  -   Aprendizaje Profundo: Los algoritmos de aprendizaje profundo ejecutan datos a través de varias capas de algoritmos de redes neuronales, las cuales pasan a         una representación simplificada de los datos a la siguiente capa.

Como se puede apreciar en la [Tabla 1](#t1) se probó la clasificación con el dataset con todos los algoritmos disponibles en weka y se puede apreciar que el algoritmo que clasifica mejor los datos de nuestro dataset es el algoritmo _Random Forest_ con un porcentaje de clasificación correcta del 74.5389 %.
## 3.  Analisis con el 80% del Dataset
  ![Imagen1](/imagenes/analisis1.png)
  
  
  Como se puede observar en la [Imagen1] se muestra los procentajes y caracteristicas con la configuracion normal del Algoritmo Random Forest,indicandonos en esta imagen que la correlacion presente es del 0.8866 dandonos a entender que sus variables guardan una  relacion estrecha de manera proporcional.
  
  ![Imagen2](/imagenes/analisis2.png)
  
  
En la [Imagen2] se observa que al trabajar solo con el 80% se ve una baja en la exactitud de clasificacion en un 2% aproximadamente, aun asi la matriz de confusion muestra un resultado aceptable en su diagonal principal.
  ![Imagen3](/imagenes/analisis3.png)
  
  
En la [Imagen3] se observa que al trabajar solo con el 80% especialmente en las variables de grasa_corporal, fuerza de agarre, longitud de sentarse y conteo de saltos se muestra una correlacion bastante fuerte indicandonos que:
  - a mayor edad, mayor grasa corporal
  - existe mucha mayor agrupacion de resultados de la fuerza del agarre de acuerdo a su edad
  - de acuerdo a la edad la mayor distancia alcanzada es alcanzada  a menor edad
  - existe una relacion negativa en las actividades de acostarse_levantarse y saltos de longitud indicandonos que a menor edad mejores resultados
## 4.  Analisis con el 20% del Dataset
En la [Imagen7] se observa que el porcentaje de instancias correctamente clasificadas es mucho menor ya que cuenta con el 68.1647% en comparacion con el 73.7513% del analisis inicial, esto se genera por que se tomo un menor numero de instancias que el original ya que este constaba con 6518 instancias y en la actual solo se tomaron en cuenta 1805. De igual forma el porcentaje de instancias incorrectamente clasificadas es mayor en el analisis del 20% ya que al existir menos datos existe un margen de error mucho mas alto.Con respecto a la matriz de confusion existe un ligero cambio en la clasificacion de las estadisticas pues en el analisis original se clasificaban de la siguiente forma C,A,B,D y en la actual con el 20% de instancias se clasifican asi C,A,D,B por lo que infiere que la clasificacion con estos datos no es muy confiable.  
  ![Imagen7](/imagenes/analisis20_1.png)
En la [Imagen8] se observa el producto del analisis de solo el 20% de los datos, en el mapa de calor nos muestra una mayor dispersion en todos los aspectos sin embargo la edad se sigue proyectando como la principal correlacion con todas las demas variables del analisis por lo que se muestra un patron mayormente marcado.
  ![Imagen8](/imagenes/analisi20_2.png)
En la [Imagen9] de igual forma se muestra el mapa de calor de la variable salto de loguitud y como esta influye en la clasificacion en correlacion con las demas variables, se puede observar que tambien existe cierto grado de dispersion pero el grado de clasificacion sigue siendo significativo.
  ![Imagen9](/imagenes/ananlisis20_3.png)
  
## 5.  Predicciones
  
En la [Imagen1] se observa
  ![Imagen1](/imagenes/prediccion_class.jpeg)
  
En la [Imagen2] se observa
  ![Imagen2](/imagenes/matrizPredicciom_class.jpeg)  
  
En la [Imagen3] se observa
  ![Imagen3](/imagenes/prediccionBF.jpeg)  

En la [Imagen4] se observa
  ![Imagen4](/imagenes/matrizBF.jpeg)  
  
En la [Imagen5] se observa
  ![Imagen5](/imagenes/prediccionPeso.jpeg)  

En la [Imagen6] se observa
  ![Imagen6](/imagenes/matrizPeso.jpeg)    

En la [Imagen7] se observa
  ![Imagen7](/imagenes/prediccionPeso.jpeg)  

En la [Imagen8] se observa
  ![Imagen8](/imagenes/matrizPeso.jpeg)  
  
En la [Imagen9] se observa
  ![Imagen9](/imagenes/grasa_visualize_error.jpeg)  

En la [Imagen10] se observa
  ![Imagen10](/imagenes/peso_visualize_error.jpeg)  
  
## 6.  Bibliografía
[1] <a name="c1">“Edad y Rendimiento Corporal - ML | Kaggle.” https://www.kaggle.com/edenniss/age-and-body-performance-ml/notebook (accessed Feb. 06, 2022).</a>

[2] <a name="c2">J. Brownlee, «How to Use Machine Learning Algorithms in Weka». 15 de julio de 2016. [En línea]. Disponible en: [https://machinelearningmastery.com/use-machine-learning-algorithms-weka/](https://machinelearningmastery.com/use-machine-learning-algorithms-weka/)</a>

[3]	<a name="c3">L. Sandoval Serrano, “Algoritmos de aprendizaje automático para análisis y predicción de datos,” pp. 36–40, 2018.</a>
