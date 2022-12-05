## 📁ESTRUCTURA
+ DATA/    # contiene los csv
+ IMG/    # contiene imagénes referentes al proyecto
+ PPTS/    # para cargar las presentaciones
+ .gitignore    # archivo para ignorar documentos
+ README.md


## 📚RECURSOS
Salaries_data.csv (Datos para trabajar)
Testeo.csv (Datos para predecir)
Muestra.csv (Ejemplo de resultados que deben subir a Kaggle)
## 🔍INFO DE COLUMNAS
+ work_year: The year the salary was paid.
+ experience_level: The experience level in the job during the year
+ employment_type: The type of employment for the role
+ job_title: The role worked in during the year.
+ salary: The total gross salary amount paid.
+ salary_currency: The currency of the salary paid as an ISO 4217 currency code.
+ salaryinusd: The salary in USD
+ employee_residence: Employee's primary country of residence in during the work year as an ISO 3166 country code.
+ remote_ratio: The overall amount of work done remotely
+ company_location: The country of the employer's main office or contracting branch
+ company_size: The median number of people that worked for the company during the year
## 📈OBJETIVO
+ Preparar los datos para los diversos modelos (proceso empírico)
+ Entrenar y Testear modelos de Machine Learning
+ Subir los resultados con el mejor modelo entrenado de Machine Learning
+ Hacer pull request con la presentación en la carpeta de 'PPTS'
+ Crear repo propio del proyecto (issue)

## PROCESO
+ Creamos una funcion que automatiza los entrenamientos de cada modelo y el ajuste de sus hyperparametros.
+ La conbinamos con el gridsearch
+ resumimos la columna de titulos de trabajo
+ Transformamos los datos de varias maneras, la transformacion de mayor exito es transformando las columnas: employee_residence, company_location, job_title, adjudicandoles a cada una un valor equivalente a los valores salariales del internet.
+ normalizamos las columnas numericas
+ metemos un label encoder para las no numericas
+ Hacemos el ttest, y entrenamos nuestra funcion automatizada que nos da los top modelos y sus hyperparametros optimos
+ Mejor resultado nos da LGBMR en kaggle aunque no es el mejor dentro de nuestra Sample. Con un MSE de 48479 con nuestro test y 35000 en kaggle

