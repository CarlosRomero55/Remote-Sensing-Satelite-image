Descripción del Modelo CNN
Objetivo: Clasificación de imágenes en 14 categorías diferentes.

Arquitectura del Modelo:

Capa Conv2D (32 filtros, tamaño de kernel 3x3):

Función: Detecta características básicas como bordes y texturas en la imagen.
Activación: ReLU (Rectified Linear Unit) para introducir no linealidad.
Capa MaxPooling2D (2x2):

Función: Reduce las dimensiones espaciales de las características, conservando las más importantes y reduciendo la complejidad computacional.
Capa Conv2D (64 filtros, tamaño de kernel 3x3):

Función: Detecta características más complejas combinando las características básicas detectadas por la capa anterior.
Activación: ReLU.
Capa MaxPooling2D (2x2):

Función: Reduce las dimensiones espaciales nuevamente, haciendo la representación de la imagen más compacta.
Capa Conv2D (128 filtros, tamaño de kernel 3x3):

Función: Detecta características aún más complejas y abstractas.
Activación: ReLU.
Capa MaxPooling2D (2x2):

Función: Reducción adicional de la dimensionalidad espacial.
Capa Flatten:

Función: Convierte las características extraídas en una sola dimensión para ser procesadas por las capas densas.
Capa Dense (512 unidades):

Función: Proporciona una capa densa para la combinación de características extraídas y permite al modelo aprender relaciones complejas entre ellas.
Activación: ReLU.
Capa Dropout (0.5):

Función: Reduce el sobreajuste (overfitting) al ignorar aleatoriamente el 50% de las unidades durante el entrenamiento.
Capa Dense (14 unidades):

Función: Proporciona las predicciones finales para cada una de las 14 clases.
Activación: Softmax, que convierte las salidas en probabilidades para cada clase.
Compilación del Modelo:

Optimizador: Adam, que ajusta los pesos del modelo de manera eficiente.
Función de Pérdida: Categorical Crossentropy, adecuada para problemas de clasificación múltiple.
Métricas: Exactitud (accuracy) para evaluar el rendimiento del modelo.
Entrenamiento y Evaluación:

Entrenamiento: Se realiza en los datos de entrenamiento con validación en un conjunto separado para ajustar y validar el rendimiento del modelo.
Evaluación: Se mide el rendimiento en el conjunto de prueba utilizando precisión, recall, F1-score y la matriz de confusión para evaluar la capacidad de clasificación del modelo.
