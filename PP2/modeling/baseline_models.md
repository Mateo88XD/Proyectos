# Reporte del Modelo Baseline

## Descripción del modelo

El modelo baseline corresponde al **Dummy Regressor**, que predice utilizando la **media** de la variable objetivo. Este modelo sirve como línea base para comparar el rendimiento de modelos más sofisticados. No utiliza patrones en los datos, por lo que cualquier modelo que supere su desempeño puede considerarse útil.

---

## Variables de entrada

Se emplearon múltiples variables predictoras que corresponden a características **numéricas** y **categóricas** del dataset.

---

## Variable objetivo

La variable objetivo es `'SalePrice'`. El **Dummy Regressor** predice simplemente la **media** de `SalePrice` sin considerar ninguna variable de entrada.

---

## Resultados de evaluación del Dummy Regressor

- **RMSE**: 56,741.89  
- **MAE**: 60,277.52  
- **R²**: 0.3581  
- **Tiempo de entrenamiento**: 1.3 s

---

## Análisis de los resultados

El modelo **Dummy Regressor** mostró un error **RMSE muy alto** (56,741.89) y un **R² de solo 0.3581**, lo que indica un **bajo poder explicativo**. Esto es esperable, ya que el modelo no considera ninguna variable de entrada para realizar sus predicciones.

Aun así, proporciona un **punto de referencia importante**: cualquier modelo que logre un **menor error** y **mayor R²** será una mejora significativa.

---

## Conclusiones

- El **Dummy Regressor** sirve como referencia para comparar modelos futuros.  
- Modelos como **Gradient Boosting**, **Random Forest** y **Ridge Regression** muestran métricas considerablemente mejores, con errores mucho más bajos (e.g., RMSE ≈ 17,090 para Gradient Boosting).  
- Esto indica que el uso de modelos más complejos es altamente recomendable para capturar patrones relevantes en los datos.

---

## Referencias

- Scikit-learn documentation: [https://scikit-learn.org](https://scikit-learn.org)  
- Evaluación de modelos de regresión: RMSE, MAE, R²  

---

## ¿Por qué usamos el Dummy Regressor como baseline?

El **Dummy Regressor** no es un modelo ganador, sino un modelo de referencia mínimo. Se considera *baseline* porque:

- No aprende nada de los datos. Solo predice valores constantes (como la media o mediana).  
- Sirve como comparación para saber si los modelos reales (como Random Forest, XGBoost, etc.) están aportando valor.  
- Es una práctica común en ciencia de datos usar este tipo de modelo como línea base.
