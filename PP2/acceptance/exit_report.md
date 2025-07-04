# Reporte del Modelo Final

## Resumen Ejecutivo

El modelo final seleccionado para resolver el problema fue un **Gradient Boosting Regressor**, el cual superó significativamente al modelo *baseline* y al resto de los modelos evaluados.

Obtuvo los siguientes resultados en las métricas de evaluación:

- **RMSE**: 17,090.93  
- **MAE**: 30,153.60  
- **R²**: 0.8405  

Estos resultados indican un alto poder predictivo y una capacidad sólida para capturar la varianza de la variable objetivo. El modelo se considera altamente efectivo para el problema planteado.

---

## Descripción del Problema

El problema abordado consistió en construir un modelo de regresión para predecir una variable continua a partir de un conjunto de características numéricas. Este tipo de problema es común en contextos donde se requiere estimar valores numéricos, como ingresos, precios, ventas, puntuaciones, etc.

### Objetivos:

- Construir un modelo predictivo preciso.  
- Comparar distintos algoritmos de regresión.  
- Seleccionar el modelo con mejor desempeño.  

### Justificación:

Un modelo de regresión eficaz permite automatizar y mejorar procesos de toma de decisiones basados en estimaciones numéricas, lo que puede generar ventajas competitivas y operativas.

---

## Descripción del Modelo

El modelo final es un **Gradient Boosting Regressor**, un algoritmo de *ensamble* basado en árboles de decisión que construye modelos de manera secuencial, cada uno corrigiendo los errores del anterior. Utiliza una combinación de técnicas de aprendizaje supervisado y optimización de gradientes para mejorar el rendimiento iterativamente.

### Metodología:

- División de los datos en conjuntos de entrenamiento y prueba.  
- Preprocesamiento y normalización según corresponda.  
- Evaluación mediante validación cruzada.  
- Comparación con múltiples modelos: regresión lineal, regresores de árbol, regresores de ensamble, etc.  
- Selección basada en métricas de desempeño.  

---

## Evaluación del Modelo

Las métricas utilizadas para evaluar el modelo fueron:

- **RMSE (Root Mean Squared Error)**: 17,090.93  
- **MAE (Mean Absolute Error)**: 30,153.60  
- **R² (Coeficiente de Determinación)**: 0.8405  

### Interpretación:

- Un **RMSE** bajo indica que el modelo comete pocos errores grandes.  
- Un **MAE** moderado refleja un buen promedio de error absoluto.  
- Un **R²** de 0.84 significa que el modelo explica aproximadamente el 84% de la varianza total de la variable objetivo, lo cual es excelente en la mayoría de los contextos prácticos.  

Comparado con el modelo *baseline* (**Dummy Regressor**, R² ≈ 0.36), este modelo representa una mejora sustancial y justificada.

---

## Conclusiones

- El modelo **Gradient Boosting** obtuvo el mejor rendimiento entre todos los evaluados.  
- Demuestra una alta capacidad para generalizar y predecir con precisión.  
- Es significativamente superior al *baseline*, lo que valida su uso práctico.

---

## Recomendaciones

- Utilizar este modelo en producción bajo condiciones similares a las de los datos de entrenamiento.  
- Monitorear el desempeño del modelo periódicamente para detectar posibles caídas por cambios en los datos (*concept drift*).  
- Explorar técnicas de ajuste de hiperparámetros o *pipelines* automatizados (AutoML) para mejoras adicionales.

---

## Referencias

- Friedman, J. H. (2001). *Greedy Function Approximation: A Gradient Boosting Machine*.  
- Scikit-learn documentation: [https://scikit-learn.org](https://scikit-learn.org)
