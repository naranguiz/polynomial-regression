## Análisis de Regresión Polinomial

Este proyecto demuestra la aplicación de regresión polinomial para analizar y predecir la expectativa de vida en base a varios indicadores socioeconómicos y relacionados con la salud. El análisis incluye preprocesamiento de datos, tratamiento de valores faltantes, escalado de características y la implementación de un modelo de regresión polinomial.

El código analiza las columnas predictoras y objetivos,  cuenta la cantidad de datos faltantes y los remplaza a través de técnicas de imputación tales como mediana por país o interpolación temporal lineal. Se hace un análisis estadístico previo y posterior a la imputación, para corroborar que la imputación no modifique indices estadísticos claves antes de aplicar el modelo de regresión polinomial.

El grado del polinomio utilizado en el modelo polinomial se elige mediante una validación cruzada del MSE. Respecto al modelo, se entrena y los resultados indican que existe una buena predicción sobre la expectativa de vida con las columnas predictoras elegidas, pero esto no es absoluto, puesto que en edades temprana (antes de los 50 años), el modelo tiene a sobre-estimar la predicción. Esto es posible debido a que las columnas predictoras tienen más relación con la expectativa de vida en personas adultas-adultas mayores y no en personas menores a 40 años. Para mejorar la predicción del modelo, se podrían considerar otras columnas predictoras que mejoren la predicción antes del rango de edad recientemente descrito. Como se mencionó anteriormente, la elección de las columnas predictoras podría mejorar a través de una regresión de Lasso u otra similar.


# Conjunto de Datos

- Expectativa de vida (variable objetivo)
- Escolaridad (años)
- Composición de ingresos de los recursos
- PIB (Producto Interno Bruto)
- Alcohol (consumo per cápita)


# Preprocesamiento de Datos
- Imputación de Valores Faltantes: Se manejaron los valores faltantes utilizando imputación por la media o mediana, según la columna.
- Escalado: Los predictores fueron estandarizados utilizando StandardScaler para normalizar los datos.

# Implementación del Modelo

- Regresión Polinomial: Se aplicó una transformación polinomial a las características para capturar relaciones no lineales.
- Entrenamiento del Modelo: El modelo fue entrenado con los datos procesados para predecir la expectativa de vida.

# Evaluación 

- Métricas de Error: El desempeño del modelo fue evaluado utilizando métricas como el Error Cuadrático Medio (MSE).
- Visualización: Se generaron gráficos para comparar la distribución de las variables clave antes y después de la imputación de valores faltantes.




