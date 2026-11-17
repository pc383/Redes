# TP4 – Redes convolucionales para clasificar lesiones de piel


El trabajo parte de un notebook proporcionado por la cátedra, que incluye el código implementado para la clasificación de imágenes dermatoscópicas del dataset ISIC, compuesto por 9 clases de lesiones de piel, mediante redes neuronales multicapa (MLP) y redes neuronales convolucionales (CNN).

El objetivo del trabajo práctico es ejecutar y comprender el código proporcionado, analizar los resultados de los distintos experimentos y completar las celdas de texto con las explicaciones y conclusiones correspondientes.

## Contenido del trabajo

El notebook `TP_04_CNN.ipynb` contiene el código proporcionado por la cátedra, los resultados de su ejecución y los análisis desarrollados para las distintas etapas del trabajo práctico:

- **Análisis exploratorio (EDA):** distribución de clases, resoluciones, características de las imágenes e identificación de duplicados.
- **Preprocesamiento:** eliminación de duplicados, división estratificada en entrenamiento, validación y prueba, y normalización de las imágenes.
- **Comparación entre MLP y CNN:** accuracy, cantidad de parámetros, tiempos de entrenamiento, generalización y robustez frente a traslaciones.
- **Arquitectura convolucional:** evaluación de diferentes cantidades de bloques, tamaños de kernel, filtros y resoluciones de entrada.
- **Overfitting y data augmentation:** análisis del sobreajuste y evaluación de distintas transformaciones de las imágenes.
- **Evaluación final:** desempeño sobre el conjunto de prueba, matriz de confusión y visualización de filtros y mapas de activación.

Las respuestas y conclusiones se desarrollaron a partir de los resultados obtenidos durante la ejecución del notebook.

## Requisitos

El trabajo fue desarrollado y ejecutado en **Google Colab**, utilizando Python y las bibliotecas indicadas en `requirements.txt`.

Para instalar las dependencias en un entorno local:

```bash
pip install -r requirements.txt
```

## Ejecución en Google Colab

1. Abrir el archivo `TP_04_CNN.ipynb` en Google Colab.

2. Ejecutar las primeras dos celdas, que descargan el repositorio original del trabajo práctico y establecen el directorio de trabajo:

   ```python
   !git clone https://github.com/cselmo/CNN-en-Skin-Dataset
   %cd /content/CNN-en-Skin-Dataset
   ```

3. Ejecutar las celdas restantes del notebook en orden.

El código utiliza las imágenes almacenadas en `data/Split_smol/`, dentro del repositorio original. Por este motivo, es necesario ejecutar las celdas iniciales antes de comenzar con el análisis.

## Metodología

El notebook identifica y elimina imágenes duplicadas antes de realizar una nueva división estratificada en conjuntos de entrenamiento, validación y prueba.

La normalización se realiza utilizando la media y el desvío estándar calculados exclusivamente sobre el conjunto de entrenamiento. Las transformaciones de *data augmentation* también se aplican únicamente a este conjunto, después de realizar la división de los datos.

Los experimentos se ejecutan utilizando tres semillas para estimar la variabilidad de los resultados. La selección de modelos se realiza a partir de las métricas de validación y el conjunto de prueba se reserva para la evaluación final.

## Archivos del repositorio

- `TP_04_CNN.ipynb`: notebook proporcionado por la cátedra, ejecutado y completado con los análisis y las respuestas a las consignas.
- `README.md`: descripción del trabajo e instrucciones para reproducirlo.
- `requirements.txt`: dependencias necesarias para ejecutar el notebook.

El repositorio no incluye el dataset ni los modelos entrenados.

## Referencia

El trabajo se desarrolló a partir del notebook y los datos proporcionados por la cátedra de Redes Neuronales del ITBA.

Repositorio original: https://github.com/cselmo/CNN-en-Skin-Dataset
