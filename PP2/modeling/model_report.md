# Elección del Mejor Modelo de Regresión - Predicción de Precios de Casas

En este análisis, se evaluaron múltiples modelos de regresión para predecir **precios de casas**. Los modelos fueron comparados utilizando métricas estándar como el **Error Absoluto Medio (MAE)**, el **Error Cuadrático Medio (MSE)**, y el **Coeficiente de Determinación (R²)**.

---

## Resumen de Resultados

| Modelo                    | Error Absoluto (MAE) | Error Cuadrático Medio (MSE) | Coef. de Determinación (R²) |
|--------------------------|----------------------|-------------------------------|-----------------------------|
| Gradient Boosting Regressor | 17,090.93             | 981,932,534.0                 | 0.8405                      |
| LightGBM                 | 17,548.04             | 988,540,355.0                 | 0.8382                      |
| Random Forest            | 18,450.86             | 1,055,867,698.0               | 0.8256                      |
| Lasso LARS               | 17,724.42             | 1,166,011,936.0               | 0.8121                      |
| Dummy Regressor          | 56,741.89             | 77,259,588.0                  | 0.0002                      |

---

## Modelo Seleccionado: **Gradient Boosting Regressor**

Este modelo fue seleccionado por obtener el **mejor desempeño general** en las métricas evaluadas. Logró el **mayor coeficiente de determinación** (**R² = 0.8405**), indicando que explica el **84% de la variación** en los datos, y presentó los **menores errores absolutos y cuadrados**, lo que demuestra su **precisión y robustez**.

---

## Conclusión

El modelo **Gradient Boosting Regressor** se considera el más adecuado para este problema, y se recomienda su uso en el despliegue o para análisis adicionales.
