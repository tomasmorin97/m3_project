# Proyecto de Machine Learning: Predicción de Precios de Diamantes
## Descripción del Proyecto
El objetivo de este proyecto es desarrollar un modelo de machine learning capaz de predecir el precio de diamantes utilizando un conjunto de datos que contiene información sobre diversas características de los diamantes.

## Datos
Los datos iniciales se encuentran en una base de datos relacional con tablas normalizadas, utilizando un identificador único (ID) como clave primaria en cada una de ellas. Estas tablas serán desnormalizadas mediante un script SQL para facilitar su análisis en un entorno de Jupyter utilizando la biblioteca pandas. El conjunto de datos contiene 10 características (features) y 40,455 registros, con el precio como la variable objetivo (target).

## Proceso de Análisis
### EDA (Análisis Exploratorio de Datos):

Se realizará un análisis exploratorio para entender la distribución de las características y la relación con el precio.
Se observará que no hay valores nulos, pero se identificarán valores 0 en las características x, y, z.
Se analizará la correlación entre las variables, destacando la fuerte correlación entre x, y, z, carat y el precio.

### Tratamiento de Datos:

Se eliminará la feature 'city' debido a que no aporta información relevante.
A pesar de la alta correlación, se mantendrán todas las variables en el modelo.
Se imputará la media de los valores en x, y, z donde sean 0, basándose en el valor de 'carat' correspondiente.

## Modelado:

Se utilizará el algoritmo Random Forest para el modelado, dado su buen desempeño en problemas de regresión.
Se realizará Cross Validation para evaluar el rendimiento del modelo.

## Validación:

Se evaluará el modelo en el conjunto de entrenamiento y en un conjunto de prueba (submission).
El modelo inicial mostrará un Root Mean Squared Error (RMSE) de 528 en el conjunto de entrenamiento y 533 en el conjunto de prueba.

## Conclusiones Preliminares
Se observa que el modelo no presenta señales de overfitting, ya que el RMSE en el conjunto de prueba es consistente con el rendimiento en el conjunto de entrenamiento.
La decisión de no escalar las variables se basa en la observación de que la información se pierde al hacerlo.
El Random Forest ha demostrado ser un modelo prometedor para este problema de regresión.

## Instrucciones para Ejecutar el Código

Ejecutar el script SQL para desnormalizar la base de datos.
Abrir el notebook de Jupyter para el análisis y modelado.
Seguir las celdas de código para el EDA, tratamiento de datos, modelado y validación.

## Requisitos del Entorno

Python 3.x
Bibliotecas: pandas, scikit-learn, matplotlib, seaborn, y cualquier otra biblioteca específica utilizada en el notebook.
