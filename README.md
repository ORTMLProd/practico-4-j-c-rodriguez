# Práctico 4

Este proyecto demuestra el proceso de ingeniería de features y preprocesamiento de datos para entrenar un modelo de aprendizaje profundo en el conjunto de datos CIFAR-10. 

El flujo de trabajo incluye pasos de preprocesamiento de datos como el cambio de tamaño y la normalización, la implementación de un patrón de transformación, la construcción y el entrenamiento de una red neuronal convolucional (CNN), el seguimiento de experimentos utilizando Weights & Biases (wandb) y la sintonización de hiperparámetros.

## Ingeniería de Características/Preprocesamiento de Datos

La ingeniería de características y el preprocesamiento de datos son pasos cruciales para preparar los datos para los modelos de aprendizaje automático. En este proyecto, realizamos los siguientes pasos:

### Preprocesamiento (resizing, normalization, etc.)

- **resizing**: Ajustar las imágenes a un tamaño consistente para asegurar la uniformidad en las dimensiones de entrada.
- **normalization**: Escalar los valores de los píxeles a un rango estándar, típicamente [0, 1], para ayudar al modelo a converger más rápido durante el entrenamiento.

Estos pasos de preprocesamiento ayudan a transformar los datos brutos en un formato adecuado para la modelización, mejorando el rendimiento y la eficiencia del entrenamiento del modelo.

### Transform Pattern

Transform Pattern implica crear una canalización de preprocesamiento que estandarice los datos de entrada antes de que sean alimentados al modelo. 
Esto asegura que los datos estén en el formato y la escala correctos, haciendo que el proceso de entrenamiento sea más eficiente.

## Modelado

En este proyecto, construimos una Red Neuronal Convolucional (CNN) utilizando TensorFlow y Keras. El modelo está diseñado para clasificar imágenes del conjunto de datos CIFAR-10, que consta de 60,000 imágenes en color de 32x32 en 10 clases diferentes.

El proceso de modelado incluye:

- **Definición de la Arquitectura del Modelo**: Construcción de una CNN con múltiples capas, incluyendo capas convolucionales, normalización por lotes, agrupación máxima, abandono y capas densas.
- **Compilación del Modelo**: Configuración del optimizador, la función de pérdida y las métricas para el modelo.
- **Entrenamiento del Modelo**: Ajuste del modelo en los datos de entrenamiento y validación en los datos de prueba.

### Seguimiento de Experimentos con wandb

El seguimiento de experimentos es esencial para mantener registros de diferentes ejecuciones del modelo, incluidas sus configuraciones, hiperparámetros y resultados. Utilizamos Weights & Biases (wandb) para rastrear nuestros experimentos. Esto nos permite monitorear el proceso de entrenamiento, comparar diferentes ejecuciones y analizar el rendimiento del modelo a lo largo del tiempo.

### Alertas de wandb

Wandb proporciona alertas para monitorear el progreso del entrenamiento y notificarte sobre cualquier evento significativo, como alcanzar una nueva mejor precisión o encontrar una caída en el rendimiento. Las alertas ayudan a mantener el control del proceso de entrenamiento y responder rápidamente a los problemas.

### Hyperparameter tuning

Hyperparameter tuning implica encontrar el mejor conjunto de hiperparámetros para el modelo. Esto puede incluir ajustar la tasa de aprendizaje, el tamaño del lote, el número de épocas y parámetros específicos de la arquitectura como el número de filtros en las capas convolucionales. Utilizamos herramientas como wandb sweeps para la optimización sistemática de hiperparámetros.
