# PREDICT THE SALARY FOR DATA JOBS


## 📈OBJECTIVO

- Preparar los datos para los diversos modelos (proceso empírico) 
- Entrenar y Testear modelos de Machine Learning
- Subir los resultados con el mejor modelo entrenado de Machine Learning


## PASOS SEGUIDOS

- Cargamos los csv de salaries y testeo
- Eliminamos las columnas de salary y salary_currency
- Concatenamos los dos data frames
- Sustituimos las columnas de experience level, employment type y company size por valores elegidos
- realizamos el label encoder en el resto de columnas
- se comprueba con 'LazyRegressor' cuál es el modelo de machine learning más adecuado
- se entrena y predice con el modelo Bagging Regressor
- se comparte el resultado en un csv en kaggle
