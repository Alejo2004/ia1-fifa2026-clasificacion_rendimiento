# Jugadores FIFA 2026

## Inteligencia Artificial I — Grupo C2 — 2026-2

Universidad Industrial de Santander (UIS)

## Integrantes

- Jose Alejandro Largo Morales — 2235162
- Santiago Garcia Pinilla — 2235159
- Johan Stevens Sánchez Aponte — 2235163

## Descripción del proyecto

Este proyecto tiene como objetivo analizar y clasificar el rendimiento de los jugadores de fútbol durante la temporada 2025/2026 mediante técnicas de inteligencia artificial y aprendizaje automático.

El rendimiento se clasifica en tres categorías: Bajo, Medio y Alto.

## Dataset

El conjunto de datos contiene 13.397 registros y 22 variables, donde cada registro representa la actuación de un jugador en un partido específico.

**Ubicación del dataset:** `data/fifa2026_player_performance_clean.csv`

El dataset puede descargarse directamente desde la carpeta `data` del repositorio.

Las seis variables predictoras seleccionadas fueron:

- Minutos jugados.
- Distancia recorrida.
- Goles.
- Asistencias.
- Tiros a puerta.
- Entradas defensivas.

## Metodología

### Análisis exploratorio de datos

- Análisis de distribuciones.
- Tratamiento de valores nulos.
- Identificación de valores atípicos.
- Análisis de correlaciones.

### Aprendizaje supervisado

Se evaluaron los siguientes modelos:

- Gaussian Naive Bayes.
- Decision Tree.
- Random Forest.
- Support Vector Machine (SVM).
- Red neuronal con Keras.

Se utilizó validación cruzada de cinco particiones agrupadas por jugador y F1 macro como métrica principal.

### Reducción de dimensionalidad

- Análisis de componentes principales (PCA).
- Comparación entre SVM original y SVM con PCA.

### Aprendizaje no supervisado

- K-Means.
- Coeficiente de silueta.
- Índice ARI.

## Resultados principales

| Indicador | Resultado |
|---|---|
| Mejor modelo supervisado | SVM |
| F1 macro en validación cruzada | 0.8215 |
| F1 macro en prueba | 0.81 aproximadamente |
| Componentes principales seleccionados | 5 |
| Varianza conservada con PCA | 96.44% |
| Número de grupos de K-Means | 6 |
| Coeficiente de silueta | 0.3405 |
| Índice ARI | 0.2986 |

## Tecnologías utilizadas

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras

## Estructura del repositorio

- `data/`: conjunto de datos utilizado.
- `notebooks/`: notebook con el desarrollo del proyecto.

## Instrucciones de ejecución

1. Descargar el notebook ubicado en la carpeta `notebooks`.
2. Descargar el dataset ubicado en la carpeta `data`.
3. Abrir el notebook en Google Colab.
4. Ejecutar las celdas en orden.
5. Cargar el archivo CSV cuando el notebook lo solicite.

## Notebook del proyecto

[Consultar notebook](notebooks/Proyecto_IA_FIFA2026.ipynb)

## Presentación final

[Consultar presentación](https://canva.link/cuskatats7w3t3g)

## Video resumen del proyecto

[Ver video del proyecto](https://drive.google.com/file/d/1VLaemD96K1ROYWerZ9Wc9T3nWF-6FEWQ/view?usp=sharing)

## Conclusiones

SVM presentó el mejor rendimiento entre los modelos supervisados evaluados.

Los minutos jugados y la distancia recorrida fueron las variables más correlacionadas con la calificación de los jugadores.

PCA permitió reducir la dimensionalidad, aunque no mejoró el rendimiento predictivo.

K-Means permitió identificar seis perfiles de rendimiento diferentes sin utilizar categorías previamente definidas.

Como trabajo futuro, se propone incorporar estadísticas específicas para cada posición, con el fin de mejorar la clasificación del rendimiento de los jugadores.