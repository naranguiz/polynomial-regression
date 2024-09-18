Regresión Polinomial aplicada a csv de la OMS: Expectativa de vida por país.

El código realiza un pre-procesamiento de los datos y elige algunas columnas escogidas arbitrariamente. Es importante mencionar que para una mejor selección de variables predictoras se debería aplicar una regresión de Lasso, la cual tomaría las mejoras columnas predictoras posibles.

El código analiza las columnas predictoras y objetivos,  cuenta la cantidad de datos faltantes y los remplaza a través de técnicas de imputación tales como mediana por país o interpolación temporal lineal. Se hace un análisis estadístico previo y posterior a la imputación, para corroborar que la imputación no modifique indices estadísticos claves antes de aplicar el modelo de regresión polinomial.

El grado del polinomio utilizado en el modelo polinomial se elige mediante una validación cruzada del MSE.

El modelo se entrena y los resultados indican que existe una buena predicción sobre la expectativa de vida con las columnas predictoras elegidas, pero esto no es absoluto, puesto que en edades temprana (antes de los 50 años), el modelo tiene a sobre-estimar la predicción. Esto es posible debido a que las columnas predictoras tienen más relación con la expectativa de vida en personas adultas-adultas mayores y no en personas menores a 40 años. Para mejorar la predicción del modelo, se podrían considerar otras columnas predictoras que mejoren la predicción antes del rango de edad recientemente descrito. Como se mencionó anteriormente, la elección de las columnas predictoras podría mejorar a través de una regresión de Lasso u otra similar.
