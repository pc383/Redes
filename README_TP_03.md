# TP3 – Redes Neuronales

## Descripción

En este trabajo práctico se implementa una red neuronal multicapa (MLP) para la clasificación de textos del dataset *20 Newsgroups*.

Se comparan diferentes técnicas de regularización y normalización, incluyendo L1, L2, Dropout, Max-Norm y Batch Normalization.

## Tecnologías utilizadas

El proyecto se desarrolló en Python, utilizando Google Colab y las siguientes bibliotecas:

- PyTorch
- Scikit-learn
- NumPy
- Pandas
- Matplotlib
- NLTK
- Optuna

## Requisitos previos

Para ejecutar el proyecto se necesita:

- Acceso a Google Colab.
- Una cuenta de Google para utilizar Google Drive.
- Las dependencias indicadas en `requirements_TP_03.txt`.

## Instalación y ejecución

1. Abrir el archivo `TP_03_Regularización.ipynb` en Google Colab.
2. Instalar las dependencias necesarias indicadas en `requirements_TP_03.txt`
3. Montar Google Drive y configurar las rutas de almacenamiento correspondientes.
4. Ejecutar las celdas del notebook en orden.



El notebook selecciona automáticamente el dispositivo de ejecución (CPU o GPU, si CUDA está disponible).

## Entrenamiento y recuperación de resultados

El notebook está organizado para permitir la ejecución de los experimentos y el análisis posterior de los resultados.

Durante el entrenamiento se guardan en Google Drive los modelos entrenados (`.pth`) y los historiales de métricas de cada época (`.csv`).

Antes de ejecutar cada experimento, el código verifica si existen resultados previamente guardados. Si están disponibles, los recupera automáticamente; de lo contrario, realiza el entrenamiento y almacena los nuevos resultados.

Esto permite volver a ejecutar el notebook para generar gráficos, comparar modelos y analizar métricas sin necesidad de repetir todos los entrenamientos.




### Uso de inteligencia artificial

Se utilizó ChatGPT (OpenAI) como herramienta de apoyo para el desarrollo del TP.
