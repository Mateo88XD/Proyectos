
# Reporte de Datos  
Este documento contiene los resultados del análisis exploratorio de datos realizado sobre los conjuntos de entrenamiento y prueba.

---

## Resumen general de los datos  
Se trabajó con dos conjuntos de datos: `df_train` (entrenamiento) y `df_test` (prueba).  
- **Observaciones**:  
  - `df_train`: 1460 registros, 81 variables  
  - `df_test`: 1459 registros, 80 variables  
- **Variables**: Ambos conjuntos contienen características numéricas y categóricas.  
- **Tipos de variables**:  
  - Numéricas: `LotArea`, `MasVnrArea`, `LotFrontage`, entre otras.  
  - Categóricas: `Neighborhood`, `MSZoning`, `SaleType`, etc.  
- **Valores faltantes**: Se identificaron valores faltantes significativos, especialmente en `LotFrontage`, `MasVnrArea` y características del sótano.  
- **Distribución de variables**: Algunas variables presentan sesgos (por ejemplo, `LotArea` y `SalePrice` están sesgadas a la derecha).

---

## Resumen de calidad de los datos  
- **Valores faltantes**:
  - Presentes en `LotFrontage`, `MasVnrArea` y múltiples variables relacionadas al sótano.
  - En `df_test` también faltan valores en `MSZoning` y `SaleType`.
- **Valores extremos**:
  - `LotArea` en `df_test` presenta valores extremadamente altos que sesgan la distribución.  
- **Errores / Duplicados**: No se han reportado errores de codificación o duplicados en esta etapa.  
- **Acciones tomadas**:
  - Identificación de columnas con alta cantidad de valores nulos para futuras imputaciones o descartes.
  - Observación de sesgos que requieren normalización o transformación para modelado.

---

## Variable objetivo: `SalePrice`  
- `SalePrice` es la variable objetivo del conjunto `df_train`.  
- **Distribución**:
  - Sesgada hacia la derecha, indicando que la mayoría de las propiedades tienen un precio moderado, pero existen algunas con precios muy altos.
- **Visualización**:
  - Histogramas y diagramas de caja utilizados para evidenciar la asimetría.
- **Consideraciones**:
  - Se recomienda aplicar transformaciones (e.g., logarítmica) para mejorar el rendimiento de modelos lineales.

---

## Variables individuales  
- **Numéricas destacadas**:
  - `LotArea`: distribución sesgada, valores extremos en `df_test`.
  - `MasVnrArea`: valores faltantes frecuentes.
- **Categóricas destacadas**:
  - `Neighborhood`: diferencias notables en frecuencia entre conjuntos de entrenamiento y prueba.
- **Transformaciones sugeridas**:
  - Aplicar normalización o log-transform a variables numéricas sesgadas.
  - Agrupamiento o codificación especial para categorías con frecuencia desigual.

---

## Ranking de variables  
- A partir del análisis de correlación (`corrwith`):
  - Varias variables numéricas presentan correlaciones relevantes con `SalePrice`.
  - No se especifican las variables con mayor correlación; se requiere inspección visual adicional de los gráficos generados.
- **Técnicas sugeridas**:
  - Correlación simple.
  - PCA para reducir dimensionalidad.
  - Importancia de características basada en modelos (por ejemplo, árboles de decisión, Random Forest).

---

## Relación entre variables explicativas y variable objetivo  
- Se utilizó análisis gráfico:
  - **Matriz de correlación**: para identificar variables numéricas fuertemente relacionadas con `SalePrice`.
  - **Diagramas de dispersión**: para visualizar relaciones individuales.
  - **Diagramas de caja (box plots)**: para evaluar el impacto de variables categóricas como `Neighborhood`.
- **Hallazgos clave**:
  - `Neighborhood` muestra fuerte impacto en `SalePrice`.
  - Diferencias en distribución entre `df_train` y `df_test` pueden afectar el rendimiento del modelo si no se tratan adecuadamente.
