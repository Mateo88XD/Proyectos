# Project Charter - Entendimiento del Negocio

## Nombre del Proyecto

**Predicción Justa de Precios de Casas**

## Objetivo del Proyecto

Desarrollar un modelo de predicción de precios de viviendas que sea **preciso y equitativo**, asegurando que variables sensibles como la **calidad de construcción** y el **barrio residencial** no introduzcan sesgos injustos en las predicciones. Este proyecto busca promover el uso ético de modelos de Machine Learning en decisiones económicas relevantes.

## Alcance del Proyecto

### Incluye:

- Limpieza y transformación de datos de precios de viviendas.
- Análisis exploratorio para detectar posibles sesgos en calidad de construcción y barrios.
- Entrenamiento y evaluación de modelos de predicción de precios.
- Implementación de métricas de equidad: **Demographic Parity Difference** y **Equal Opportunity Difference**.
- Documentación completa bajo la metodología TDSP.
- Uso de MLflow para seguimiento de experimentos y Fairlearn para evaluación de fairness.

### Excluye:

- Despliegue en producción en sistemas externos.
- Recolección de nuevos datos fuera del dataset provisto.
- Análisis financiero o regulatorio de precios de viviendas.

## Metodología

Se seguirá la metodología **TDSP (Team Data Science Process)**, abarcando las fases de Entendimiento del Negocio, Adquisición y Exploración de Datos, Modelado, Evaluación de Fairness, y Entrega Final. Se utilizarán herramientas como **Python**, **Scikit-learn**, **MLflow**, **Fairlearn**, **Jira** y **GitHub**.

## Cronograma

**Duración total: ≈2 meses** (del 14 de abril al 20 de junio de 2025)

| Etapa | Duración Estimada | Fechas | Entregables Asociados |
|:------|:------------------|:-------|:----------------------|
| Definición del problema (investigación, Project Charter, Jira, estructura GitHub) | 2 semanas | del 14 de abril al 28 de abril | Evidencia N°1: Definición del problema |
| Análisis exploratorio de datos (EDA) y Fairlearn (análisis técnico y ético) | 1 semana | del 29 de abril al 5 de mayo | Documento "data_definition" + Notebook de EDA + Informe de hallazgos |
| Preparación de los datos (limpieza, codificación, balanceo, feature engineering) | 1 semana | del 6 de mayo al 12 de mayo | Documento "data_summary" + Script de preprocesamiento + Dataset procesado + Informe ético |
| Modelado inicial y experimentación (entrenamiento y tracking con MLflow) | 1 semana | del 13 de mayo al 16 de mayo | Evidencia N°2: Modelado y experimentación |
| Evaluación de modelos, mejora y selección final | 1 semana | del 17 de mayo al 23 de mayo | Documentos "baseline_models" y "model_report" actualizados |
| Despliegue del modelo en entorno de producción (API local con MLflow) | 2 semanas | del 24 de mayo al 6 de junio | Evidencia N°3: Despliegue del modelo en producción |
| Documentación final (DeploymentDoc y ExitReport) + Cierre del proyecto | 2 semanas | del 7 de junio al 20 de junio | Entrega final de toda la documentación y repositorio completo |

---

### Resumen de Entregables y Fechas Límite

- **Evidencia N°1: Definición del problema** → *Fecha límite:* 28/04/2025
- **Evidencia N°2: Modelado y experimentación** → *Fecha límite:* 16/05/2025
- **Evidencia N°3: Despliegue del modelo en producción** → *Fecha límite:* 06/06/2025

---

**Notas:**

- El proyecto debe seguir las fases de la metodología **TDSP**.
- Se debe usar **MLflow** para tracking de experimentos y **Fairlearn** para evaluar equidad.
- Todo el proceso y entregables deben ser versionados en **GitHub**.
- El despliegue será en entorno **local**, no se requiere despliegue en producción pública.

## Equipo del Proyecto

- **Project Manager:** Paola Navarro — Planificación, organización de tareas, control de entregables.
- **Data Engineer:** Gerardo Agustín Galeano — Limpieza, transformación y estructura de datasets.
- **Data Scientist:** Sergio Daniel Almada — Entrenamiento y evaluación de modelos predictivos.
- **Data Analyst:** Mateo Beltramone — Exploración y análisis de datos para identificar patrones, tendencias y generar insights accionables.
- **Data Analyst:** Nahir Dayana Guzmán — Exploración y análisis de datos para identificar patrones, tendencias y generar insights accionables.
- **Ethical Reviewer:** Giuliana Gesto — Análisis de fairness y equidad en modelos.

## Presupuesto Estimado (Pesos Argentinos - ARS)

Este presupuesto estima los costos asociados al proyecto, incluyendo una estimación del valor del tiempo dedicado por los roles clave del equipo.

| Recurso / Actividad                     | Unidad de Medida | Cantidad | Costo Estimado por Unidad (ARS/semana por rol) | Total Estimado (ARS) | Notas                                                                                                                               |
| :-------------------------------------- | :--------------- | :------- | :--------------------------------------------- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| **Project Management** | Semana           | 8        | 150,000                                       | 1,200,000            | Estimación del valor del tiempo dedicado por el Project Manager.                                                                    |
| **Data Engineering** | Semana           | 4        | 180,000                                       | 720,000              | Estimación del valor del tiempo dedicado por el Data Engineer. Mayor dedicación inicial.                                            |
| **Data Science** | Semana           | 4        | 200,000                                       | 800,000              | Estimación del valor del tiempo dedicado por el Data Scientist. Mayor dedicación en las fases de modelado y evaluación.             |
| **Data Analysis (Equipo)** | Semana           | 2 (cada uno) | 160,000                                       | 640,000              | Estimación del valor del tiempo dedicado por el equipo de Data Analysts (considerando la dedicación principal en la fase inicial). |
| **Ethical Review** | Semana           | 2        | 170,000                                       | 340,000              | Estimación del valor del tiempo dedicado por el Ethical Reviewer. Dedicación en fases clave.                                      |
| **Infraestructura Cloud (Estimado)** | Mes              | 2        | 50,000                                        | 100,000              | Costos estimados por uso de plataformas para cómputo y almacenamiento (si aplica).                                                    |
| **Licencias de Software (Estimado)** | Único            | 1        | 20,000                                        | 20,000               | Costos estimados por licencias de herramientas específicas (si aplica).                                                              |
| **Adquisición de Datos Adicionales (Opcional)** | Único        | 1        | 100,000                                       | 100,000              | Presupuesto en caso de necesitar fuentes de datos externas (no incluido en el alcance actual).                                     |
| **Herramientas y Librerías Premium (Opcional)** | Único      | 1        | 30,000                                        | 30,000               | Costos estimados por licencias de herramientas o librerías especializadas (no requeridas inicialmente).                                |
| **Imprevistos (10% del total)** | Único            | 1        | -                                             | 395,000              | Reserva para cubrir cualquier costo inesperado.                                                                                    |
| **TOTAL ESTIMADO DEL PROYECTO** |                  |          |                                                 | **4,345,000** |                                                                                                                                    |

**Nota:** Este presupuesto incluye una estimación del valor del tiempo dedicado por los roles clave del equipo. Los costos por semana por rol son una estimación basada en salarios promedio en Argentina.

## Stakeholders

- **Equipo de Ciencia de Datos:** Responsable del desarrollo técnico y documentación del proyecto.
- **Usuarios Finales:** Compradores, vendedores y agentes inmobiliarios interesados en estimaciones justas de precios.
- **Revisor Ético:** Supervisión de métricas de equidad y recomendaciones de mejora.
- **Project Manager:** Seguimiento y control del avance del proyecto.

### Expectativas de los Stakeholders

- Obtener un modelo que prediga precios con **alta precisión** (RMSE < 30,000, R² > 0.8).
- Validar que las predicciones sean **justas** respecto a calidad de vivienda y barrio (Demographic Parity Difference < 0.1).

## Aprobaciones

- **Aprobador del Proyecto:** Paola Navarro, Project Manager
- **Firma:** Paola Navarro
- **Fecha de Aprobación:** 28/4/25
