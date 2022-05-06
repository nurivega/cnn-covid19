# cnn-covid19
En el presente proyecto se encuentra la implementacion de una red neuronal convolucional binaria entrenada con imagenes de radiografias de tórax con signos de covid-19 y radiografias de tórax de pacientes sin ninguna afeccion pulmonar. Ademas, se implementa una matriz de confusion con la finalidad de poder analizar el desempeño de la red entrenada. 
La red entrenada lgró clasificar radiografias de tórax con signos de covid-19 con un 79% de exactitud sobre el conjunto de prueba.
El conjunto de datos utilizado en este proyecto fue generado a partir del dataset publicado en la siguiente página: https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database

Implementacion: 
entrenar.py : En el mismo se implementa la red completa, la misma es entrenada utilizando las imagenes guardadas en data/entrenamiento, al mismo tiempo, valida el entrenamiento de la misma utilizando las imagenes de data/validacion. Por ultimo, genera un grafico de entrenamiento comparando la exactitud y el error del conjunto de enetrenamiento contra el conjunto de validación.
predecir.py : Utiliza el modelo y los pesos de la red entrenada para predecir la clase de la imagen específica que se le indica. La clasficiacion se realiza de manera individual
confusionMatrix.py : Este algoritmo implementa una matriz de confusion, la misma se genera a partir de las imagenes de prueba que se encuentran en la carpeta especifica para este fin (/data/prueba). Como resultado se obtiene una matriz de confusion con la clasificacion de todas las imagenes del conjunto de prueba, permite visualizar los falsos negativos y falsos positivos.

Distribucion de carpetas: 
Diseño: Dentro de ella se encuentra el diseño de la arquitectura de la red. 
Resultados : en esta carpeta se encuentran los resultados del entrenamiento y la matriz de confusion generada. 
Modelo : En ella se encuentra el modelo y los pesos de la red entrenada. 
Data : En esta carpeta se guardan las imagenes utilizadas para el entrenamiento, la validación y las pruebas. 
