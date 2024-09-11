# Proyecto: Clustering de Imágenes con KMeans, Clustering Jerárquico y Gaussian Mixtures

## Descripción

Este proyecto implementa diferentes algoritmos de **clustering** para analizar y procesar una imagen. Utiliza tres enfoques principales: **KMeans**, **Clustering Jerárquico** y **Gaussian Mixtures**, con el objetivo de reducir la paleta de colores de una imagen, segmentarla en grupos de colores similares y recomponerla utilizando una paleta reducida.

### Objetivos del Proyecto:
- Aplicar diferentes algoritmos de clustering a una imagen.
- Obtener una paleta de colores reducida para mejorar el rendimiento.
- Comparar los resultados visuales entre los algoritmos.
- Evaluar la eficiencia y calidad visual de cada enfoque.

## Estructura del Proyecto

El proyecto está organizado de manera modular y clara para facilitar la escalabilidad y mantenibilidad. A continuación, se describe la estructura de carpetas:


# image-clustering-lab

Este proyecto se enfoca en la segmentación de imágenes utilizando diferentes algoritmos de clustering.

## Estructura del Proyecto

```plaintext
image-clustering-lab/
├── data/                         # Carpeta que contiene la imagen de entrada
│   └── image.jpg                 # Imagen original utilizada para el análisis
├── notebooks/                    # Notebooks de Jupyter para la ejecución del proyecto
│   └── image_clustering.ipynb    # Notebook que contiene el flujo completo del análisis
├── output/                       # Carpeta de salida para las imágenes generadas
│   ├── reconstructed_image_gmm.jpg       # Imagen recombinada utilizando Gaussian Mixtures
│   ├── reconstructed_image_hierarchical.jpg # Imagen recombinada utilizando Clustering Jerárquico
│   └── reconstructed_image_kmeans.jpg     # Imagen recombinada utilizando KMeans
├── src/                          # Código fuente del proyecto
│   ├── __init__.py               # Permite que src sea un paquete de Python
│   └── image_clustering.py       # Módulo que contiene las funciones principales de clustering
├── venv/                         # Entorno virtual de Python
├── .gitignore                    # Archivo que excluye archivos innecesarios del repositorio
├── README.md                     # Archivo de documentación del proyecto
├── requirements.txt             # Dependencias y bibliotecas necesarias para el proyecto
└── .gitignore                    # Archivo para excluir archivos no deseados del control de versiones


## Aplicar KMeans:

from src.image_clustering import apply_kmeans
labels, palette = apply_kmeans(pixels, n_clusters=6)

## Recomponer la imagen:

from src.image_clustering import reconstruct_image
reconstructed_image = reconstruct_image(labels, palette, image_resized.shape)

## Comparación de Algoritmos
El proyecto implementa tres algoritmos de clustering, cada uno con características y resultados visuales diferentes:

** KMeans:** Rápido y eficiente, pero puede no capturar detalles sutiles en la imagen.
** Clustering Jerárquico: ** Captura relaciones jerárquicas entre los datos, pero es más costoso en términos de tiempo y memoria.
** Gaussian Mixtures: ** Proporciona una representación más suave y probabilística, ideal para segmentar imágenes con transiciones graduales de color.
Resultados Visuales
Los resultados de la recomposición de la imagen se encuentran en la carpeta output/. A continuación, un ejemplo de los resultados visuales:

* Imagen con KMeans:

* Imagen con Clustering Jerárquico:

* Imagen con Gaussian Mixtures:

## Contribuciones
Este proyecto es un ejercicio académico y abierto a mejoras. Si deseas contribuir, siéntete libre de realizar un fork del repositorio y enviar pull requests.
