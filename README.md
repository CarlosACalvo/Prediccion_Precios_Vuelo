# <font color='orange'><center>🛫 **Predicción del Precio de Vuelos en India** 🛬</center></font>

<a href="https://github.com/CarlosACalvo/Prediccion_Precios_Vuelo/blob/main/Prediccion_Precios_Vuelos.ipynb" target="_blank">
  <img src="https://img.shields.io/badge/Ver_Notebook-GitHub-blue?logo=github" alt="Open In GitHub"/>
</a>
<br><br>
<a href="https://colab.research.google.com/github/CarlosACalvo/Prediccion_Precios_Vuelo/blob/main/Prediccion_Precios_Vuelos.ipynb" target="_blank">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## 🔮 Descripción
Modelo de machine learning para predecir precios de vuelos en India basado en múltiples variables como aerolínea, ruta, hora, clase, entre otras. 

El proyecto implementa en realidad tres modelos diferentes: RandomForest, XGBoost y CatBoost, y compara el desempeño de los mismos además de hacer una ligera optimización de hiperparámetros. 

Como objetivo final se elige el modelo que mejor desempeño haya demostrado y se implementa una predicción con un pequeño set de datos no-conocidos por el modelo, lo cuales son luego validados para verificar que sean razonables de acuerdo a las características de los datos de entrada, y se comprueban comparándolos con datos históricos similares.

## 🧩 Características
- Análisis exploratorio de datos (EDA)
- Preprocesamiento y limpieza de datos
- Implementación de 3 modelos de ML
- Optimización de hiperparámetros
- Evaluación comparativa de modelos
- Sistema de predicción de precios

## ⁉️ Variables Analizadas
- Aerolínea
- Origen y destino
- Fecha y hora del vuelo
- Clase (Economy/Business)
- Número de escalas
- Duración del vuelo en minutos

## 🤯 Tecnologías Utilizadas
- Python 3.13
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- CatBoost
- Matplotlib
- Seaborn

## 📚 Estructura del Proyecto
1.   Definición del problema
2.   Importación de Librerías y Carga de Datos
3.   Reporte de calidad de los datos
4.   Análisis exploratorio de los datos
5.   Análisis de correlaciones
6.   Transformaciones necesarias
7.   Elección y creación de modelos
8.   Métricas de evaluación
9.   Optimización con Grilla de hiperparametros
10.   Ejemplo de Predicción de Precios
11.   Conclusión Final

## 📊 Algunas Visualizaciones
![tres](https://github.com/user-attachments/assets/a115d61a-585f-411d-81fd-7e33b1b4711f)

![dos](https://github.com/user-attachments/assets/ed57093e-3e72-4a81-be2d-fa8137674088)

![uno](https://github.com/user-attachments/assets/31bb4747-bf43-4317-a769-25579c6174f3)

## 🏅 Comparación de Modelos

| Modelo | MSE | R² | MAE |
|--------|-----|-------|-----|
| Random Forest | 1.30e+07 | 0.975 | 2,200.99 |
| XGBoost | 1.69e+07 | 0.967 | 2,733.70 |
| CatBoost | 9.86e+06 | 0.981 | 1,788.83 |

> El modelo **CatBoost** obtuvo el mejor desempeño con:
> - El menor Error Cuadrático Medio (MSE): 9.86e+06
> - El mayor coeficiente de determinación (R²): 0.981
> - El menor Error Absoluto Medio (MAE): 1,788.83

## 🧙🏻‍♂️ Ejemplos de predicciones

Las predicciones realizadas son:

| 	Ruta	| Aerolínea	| Clase |	Precio Predicho |
|---------|-----------|--------|-----------------|
|	Delhi_Mumbai |Vistara	| Business	| ₹30,558.62 |
|	Mumbai_Kolkata |	Air India	| Economy |	₹4,464.27 |
|	Kolkata_Delhi	| SpiceJet	| Economy |	₹5,988.87 |

💵 Análisis de la razonabilidad de los precios predichos

--------------------------------------------------

    * Validando: Delhi_Mumbai - Vistara - Business - Mañana - $30558.62

	Precio mínimo: $28,872.00
	Precio máximo: $90,281.00
	Precio promedio: $48,902.89
	Cantidad de vuelos similares: 785

    * Validando: Mumbai_Kolkata - Air India - Economy - Tarde - $4464.27

	Precio mínimo: $4,457.00
	Precio máximo: $21,273.00
	Precio promedio: $7,573.19
	Cantidad de vuelos similares: 331

    * Validando: Kolkata_Delhi - SpiceJet - Economy - Noche - $5988.87

	Precio mínimo: $3,999.00
	Precio máximo: $22,327.00
	Precio promedio: $6,086.34
	Cantidad de vuelos similares: 121

 Se observa que todos los precios predichos están razonablemente en el rango de los precios de otros vuelos históricos con las mismas características.

## 🧑🏻‍🦱 Autor
[Carlos Andrés Calvo G.]

## 🪪 Licencia
Este proyecto está bajo la Licencia GNU-GPLv3 - ver el archivo LICENSE.md para más detalles.
