# Análisis de un Perceptrón Multicapa (MLP) para Reconocimiento de Patrones

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

Este repositorio contiene la implementación desde cero (sin librerías de Deep Learning de alto nivel) de una Red Neuronal **Perceptrón Multicapa (MLP)**. El proyecto fue desarrollado como Trabajo Práctico Integrador para la cátedra de **Inteligencia Artificial** (5º Nivel ISI) en la **Universidad Tecnológica Nacional, Facultad Regional Resistencia (2025)**.

## Descripción del Proyecto

El objetivo principal de este proyecto es comprender en profundidad los mecanismos internos de una red neuronal. Para ello, se implementó el algoritmo de **Retropropagación del error (Backpropagation)** con término de **Momento** utilizando únicamente `NumPy` para los cálculos matriciales.

La red fue entrenada para resolver un problema de clasificación de patrones visuales: reconocer las letras **"b"**, **"d"** y **"f"** representadas en una cuadrícula de 10x10 píxeles (100 entradas), incluso cuando estas presentan distorsión o ruido.

### Resultados Destacados
Según el análisis realizado en el informe final:
* **Precisión:** El modelo final optimizado alcanzó una precisión del **98%** en el conjunto de validación.
* **Arquitectura Óptima:** Se determinó que una configuración de 2 capas ocultas con una tasa de aprendizaje de 0.1 y momento de 0.9 ofreció el mejor balance entre convergencia y generalización.

## Características Principales

* **Implementación "From Scratch":** Todo el motor de la red neuronal (`forward`, `backward`, `update`) está escrito en Python puro y NumPy, permitiendo una comprensión granular del algoritmo.
* **Configuración Flexible:** La clase `MLP` permite definir arbitrariamente la arquitectura (cantidad de capas y neuronas) y las funciones de activación (Sigmoide, Lineal).
* **Generación de Datasets:** Scripts para generar conjuntos de datos sintéticos con niveles controlados de ruido (inversión de píxeles del 1% al 30%).
* **Interfaz Gráfica Interactiva:** Incluye una GUI integrada en el notebook (usando `ipywidgets`) que permite dibujar o distorsionar patrones en tiempo real y ver la predicción de la red.

## Tecnologías Utilizadas

* **Lenguaje:** Python 3
* **Entorno:** Jupyter Notebook / Google Colab
* **Librerías Principales:**
    * `numpy`: Operaciones matriciales y matemáticas.
    * `pandas`: Manejo de datasets (CSV).
    * `matplotlib`: Visualización de curvas de error (MSE).
    * `scikit-learn`: Únicamente para `OneHotEncoder` y división de datos (`train_test_split`).
    * `ipywidgets`: Interfaz de usuario interactiva.
    * `tqdm`: Barras de progreso durante el entrenamiento.

## Estructura del Repositorio

```text
├── MLP.ipynb                  # Notebook principal: Clase MLP, Entrenamiento y GUI
├── Generacion_datasets.ipynb  # Notebook para crear los datos de entrenamiento (b, d, f)
└── Informe-MLP.pdf            # Documentación académica detallada y análisis de resultados
```
## Instalación y Uso

> **⚠️ Recomendación:** Para asegurar el correcto funcionamiento de la interfaz gráfica y las barras de progreso, se recomienda encarecidamente ejecutar este proyecto en **Google Colab**.

### Opción A: Google Colab (Recomendado)

1.  **Descargar Archivos:** Descarga los notebooks `MLP.ipynb` y `Generacion_datasets.ipynb` de este repositorio.
2.  **Subir a Colab:** Sube ambos archivos a tu Google Drive o ábrelos directamente en [Google Colab](https://colab.research.google.com/).
3.  **Generar Datos:**
    * Abre `Generacion_datasets.ipynb` y ejecuta todas las celdas.
    * Esto generará los archivos `.csv` en el almacenamiento de sesión.
4.  **Entrenar y Probar:**
    * Abre `MLP.ipynb`.
    * Asegúrate de que los archivos `.csv` generados en el paso anterior estén accesibles (si se borraron al cambiar de notebook, súbelos manualmente a la carpeta de archivos de la izquierda en Colab).
    * Ejecuta todas las celdas (`Runtime` > `Run all`) para entrenar el modelo y desplegar la interfaz de dibujo al final.

### Opción B: Ejecución Local

Si prefieres ejecutarlo en tu máquina, necesitarás Jupyter Notebook instalado:

1.  Clona el repositorio:
    ```bash
    git clone [https://github.com/tu-usuario/nombre-del-repo.git](https://github.com/tu-usuario/nombre-del-repo.git)
    ```
2.  Instala las dependencias:
    ```bash
    pip install numpy pandas matplotlib scikit-learn tqdm ipywidgets
    ```
3.  Ejecuta los notebooks en el mismo orden descrito arriba (primero Generación, luego MLP).

## Autores - Grupo "Tortugas V2"

* **Lucas Baggio**
* **Rodrigo Cordoba**
* **Lucas Gauna Lesteyme**
* **Enzo Gonzalez Urbieta**
* **Rafael Lezcano**

## Licencia y Descargo

Este proyecto es de carácter académico y educativo para la cátedra de Inteligencia Artificial de la UTN-FRR. El código se proporciona con fines de demostración de los conceptos aprendidos.

---
*UTN - Facultad Regional Resistencia - Ingeniería en Sistemas de Información - 2025*
