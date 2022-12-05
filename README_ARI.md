# Proyect5_kaggle_Ari
![salary-negotiations](https://user-images.githubusercontent.com/113017465/205659890-6c6c26b4-2340-4305-85b5-3872793c31c3.jpg)


# OBJETIVO:
Este proyecto consisite en participar en una competición de Kaggle para intentar crear un modelo de aprendizaje automático (Machine Learning) sobre predicción de salarios.

¿El objetivo?como en toda competición, ganar💪 ...¿Cómo?🤷‍♀️ Creando el modelo con menor error posible.

# PROCEDIMIENTO:

Se nos dan dos dataset, uno con los datos para trabajar (salary) y otro con los datos para predecir(testeo), el proceso llevado a cabo fue el siguiente:

-  DATASET DE TRABAJO: EN este llevaré a cabo el proceso de limpieza, calculos de correlación, eliminación de columnas carentes de interés, modificación de columnas categóricas a numéricas, normalización y llevo a cabo el proceso de entrenamiento, predicciones y testeo con las modificaciones realizadas.

-  DATASET PARA PREDECIR: Una vez realizado los entrenamientos y testeos, realizo las mismas modificaciones en este dataset para poder subirlo a la competición.

### RESUMEN DE LOS PROCESOS REALIZADOS:
-  Mi dataset de trabajo se puede dividir en dos, en ambos eliminé las columnas de 'salary' y 'salary_currency' además de dividir mi dataframe en X e Y, estableciendo como mi Y la columna de 'salary_in_usd', no obstante, en uno realicé la conversión de categóricas a numéricas con LabelEncode y sin normalizar, y en el otro con GetDummies y normalizando.

-  Entreno ambos con varios modelos de regresión para poder elegir el más adecuado una vez tenga los resultados.

-  Entreno los modelos con el 80% de los datos totales del dataset y hago la predicción con X_test, que es el 20% del dataset train, obteniendo el error cuadrático medio.

-  Me quedo con los 3 mejores modelos que serían los que tienen menor error cuadrático medio, en mi caso serián Lasso, Ridge y LGBMRegressor, y el dataset que mejor funciona sin duda es el de getdummies. 
  
-  Hago la predicción con el testeo.
  
-  Relizo la submission, curiosamente en la competición mi mejor resultado es aquel que obtengo con Lasso, pese a que no es el procedimiento con el que obtengo un MSE menor.


# RECURSOS UTILIZADOS:
Kaggle data set

Librarias:

Pandas-Numpy-Sklearn
