# Project Kaggle Competition - SALARY PREDICTION

<img src="https://github.com/AnaChaparro/Kaggle_Competition/blob/main/img/bank-number-usa-bills-dollar.jpg?raw=true"> 

## Tabla de contenido:
1. [Introducción](#introducción)
2. [Exploración de los datos](#exploración-de-los-datos)
3. [Limpieza y transformación](#limpieza-y-transformación)
4. [Machine Learning](#machine-learning)
5. [Resultados](#resultados)


### 1. Introducción

Se ha realizado el siguiente proyecto que trata de una competición de Kaggle en la que mediante modelos de Machine Learning y una base de datos basada en salarios de diferentes empresas y puestos de trabajo, hay que determinar que modelo puede predecir de la mejor manera el salario en USD que depende de determinadas variables.

Los datos iniciales se tratan de la tabla de salaries, testeo y muestra. Con la tabal de salaries de hará la predición para constrastarse con la de testeo. La de muestra simplemente indica el formato en el que los datos han de subirse a Kaggle.

### 2. Exploración de los datos

En este apartado se hace un balance de la consistencia de los datos, se estudia cual es la variable a predecir y se hace un estudio del resto de variables que aparecen en las columanas, tomándose la decisión de eliminar salary y salary_currency, ya que la variable a precedir es salary_in_usd. En el README únicamente se va a tener en cuenta el modelo que ha ofrecido mejor puntuación en la web de Kaggle, por lo que únicamente nos referenciaremos a este.

### 3. Limpieza y transformación

Los datos vienen dados de manera bastante consistente y limpia, por lo que únicamente se ha decidido realizar algunas tranformaciones. Cabe decir que todos las tranformaciones realizadas al csv de salaries, se han aplicado también al testeo, concatenando inicialmente ambos dataframes, y separándolos para realizar la comprobación de los modelos.

Tras eliminar las columnas indicadas en el apartado anterior, se ha realizado la locaización de outliers, y eliminado las filas que los contenían, y se ha eliminado la columna de employee_residence. Posteriormente se ha realizado el get dummies de las columnas categóricas ('experience_level','employment_type', 'job_title','company_location','company_size') y se han normalizado las columas de work_year y remote_ratio.
Toda vez realizados estos cambios, se han separado los DF de salaries y testeo y se ha realizado el train test split en partiendo el DF de salaries en 80 y 20%.

### 4. Machine Learning

Una vez se tienen los datos limpios y transformados se entrenan y se predice con los siguientes modelos:

- LinearRegression
- Lasso       
- Ridge        
- ElasticNet
- Support Vector Regressor (SVR)
- Random Forest Regressor(RFR)
- Extra Tree Regressor (ETR)
- Gradient Boosting Regressor (GBR)
- XGB Regressor (XGBR)
- Cat Boost Regressor (CTR)
- LGBM Regressor (LGBMR)

### 5. Resultados

Una vez se ha realizado la predicción con todos los modelos indicados, se calcula el RMSE y el R2 de cada modelo para ver cual predicón se ajusta más.
En este caso el modelo que ofrece un menor error, en principio, ya que no disponemos de todos los datos para realizar la comprobación, sería el modelo Ridge habiendo sido entrenado con el 100% de los datos de salaries.

