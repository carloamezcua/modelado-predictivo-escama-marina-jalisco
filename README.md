# Modelado predictivo de escama marina en Jalisco

Proyecto de análisis, limpieza y modelado predictivo sobre la pesquería de escama marina en Jalisco, con datos del periodo 2010-2021. El objetivo principal es predecir la biomasa desembarcada (`PesoVivoKg`) y entender qué variables explican mejor su comportamiento.

## Resumen del proyecto

El trabajo se desarrolla en el notebook [Escama_Marina.ipynb](Escama_Marina.ipynb) y sigue un flujo completo de ciencia de datos:

1. Carga y resguardo del dataset original.
2. Inspección estructural y validación de reglas de negocio.
3. Limpieza de registros inconsistentes y reducción de columnas irrelevantes.
4. Normalización de tipos de datos y tratamiento de categorías raras.
5. Análisis exploratorio con estadísticos, histogramas, boxplots y mapas de calor.
6. Preparación de variables para modelado con codificación one-hot y escalado.
7. Entrenamiento y comparación de tres modelos: Random Forest, SVM y Regresión Polinómica.

## Datos

El repositorio incluye el archivo [escama_marina_Jalisco_2010-2021.csv](escama_marina_Jalisco_2010-2021.csv), que se usa como base para el análisis.

Durante el notebook se construyen versiones limpias y agregadas del dataset para facilitar el modelado y reducir ruido. También se generan variables derivadas como el año centrado y se agrupan categorías poco frecuentes bajo la etiqueta `OTROS`.

## Objetivo analítico

El objetivo es estimar la biomasa de captura y evaluar qué factores tienen mayor peso en la predicción. Entre las variables revisadas aparecen el esfuerzo pesquero, el tiempo efectivo, el precio, el mes, el sitio de desembarque y la especie.

## Modelos evaluados

El notebook compara tres enfoques de regresión:

1. Random Forest Regressor.
2. Support Vector Regressor (SVR).
3. Regresión Polinómica de grado 2.

Además, se evalúa una variante con transformación logarítmica del objetivo para reducir el efecto de valores extremos y mejorar la estabilidad de algunos modelos.

## Principales etapas del notebook

El notebook está organizado en estas secciones:

1. Carga de datos.
2. Inspección inicial.
3. Limpieza.
4. Preparación para modelado.
5. Modelado.

En el proceso se incluyen diagnósticos de duplicados, correlación numérica, asociación entre variables categóricas, multicolinealidad con VIF y visualizaciones comparativas para apoyar la interpretación.

## Requisitos

El análisis está pensado para ejecutarse en un entorno Python con librerías de ciencia de datos como:

1. pandas
2. numpy
3. matplotlib
4. seaborn
5. scipy
6. scikit-learn
7. statsmodels

## Cómo usarlo

1. Abre [Escama_Marina.ipynb](Escama_Marina.ipynb) en Jupyter o VS Code.
2. Verifica que el archivo de datos esté disponible en la ruta que usa el notebook o actualiza la variable de carga al inicio.
3. Ejecuta las celdas en orden.
4. Revisa las tablas y gráficas generadas en cada etapa para interpretar la limpieza y el desempeño de los modelos.

## Resultados esperados

Al finalizar el notebook deberías tener:

1. Un dataset limpio y preparado para modelado.
2. Un conjunto de variables numéricas y categóricas transformadas para aprendizaje automático.
3. Métricas comparables de los tres modelos.
4. Una recomendación final basada en el menor error y el mejor ajuste relativo.

## Nota

El notebook fue diseñado para trabajo exploratorio y puede requerir ajustar rutas locales de lectura o escritura antes de ejecutarlo en otra máquina.
