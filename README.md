# Máster Data Science - Deep-learning

## Actividad 1: Redes Densas
Para esta primera actividad vamos a utilizar el wine quality dataset. Con el que trataremos de predecir la calidad del vino.
La calidad del vino puede tomar valores decimales (por ejemplo 7.25), independientemente de que en el dataset de entrenamiento sean números enteros. Por lo tanto, el problema es una regresión.

| fixed acidity | volatile acidity | citric acid | residual sugar | chlorides | free sulfur dioxide | total sulfur dioxide | density | pH   | sulphates | alcohol | quality |
|---------------|------------------|-------------|----------------|-----------|---------------------|----------------------|---------|------|-----------|---------|---------|
| 7.4           | 0.70             | 0.00        | 1.9            | 0.076     | 11.0                | 34.0                 | 0.9978  | 3.51 | 0.56      | 9.4     | 5       |
| 7.8           | 0.88             | 0.00        | 2.6            | 0.098     | 25.0                | 67.0                 | 0.9968  | 3.20 | 0.68      | 9.8     | 5       |
| 7.8           | 0.76             | 0.04        | 2.3            | 0.092     | 15.0                | 54.0                 | 0.9970  | 3.26 | 0.65      | 9.8     | 5       |
| 11.2          | 0.28             | 0.56        | 1.9            | 0.075     | 17.0                | 60.0                 | 0.9980  | 3.16 | 0.58      | 9.8     | 6       |
| 7.4           | 0.70             | 0.00        | 1.9            | 0.076     | 11.0                | 34.0                 | 0.9978  | 3.51 | 0.56      | 9.4     | 5       |

#### Cuestión 1: Cree un modelo secuencial que contenga 4 capas ocultas(hidden layers), con más de 60 neuronas por capa, sin regularización y obtenga los resultados.

#### Cuestión 2: Utilice el mismo modelo de la cuestión anterior pero añadiendo al menos dos técnicas distinas de regularización. No es necesario mejorar el loss.
Ejemplos de regularización:  [Prevent_Overfitting.ipynb](https://github.com/ezponda/intro_deep_learning/blob/main/class/Fundamentals/Prevent_Overfitting.ipynb)

#### Cuestión 3: Utilice el mismo modelo de la cuestión anterior pero añadiendo un callback de early stopping. No es necesario mejorar el loss.

#### Cuestión 4: ¿Podría haberse usado otra función de activación de la neurona de salida? En caso afirmativo especifíquela.
#### Cuestión 5: ¿Qué es lo que una neurona calcula?
#### Cuestión 6: ¿Cuál de estas funciones de activación no debería usarse en una capa oculta (hidden layer)?
#### Cuestión 7: ¿Cuál de estas técnicas es efectiva para combatir el overfitting en una red con varias capas ocultas? Ponga todas las que lo sean.
a) Dropout
b) Regularización L2.
c) Aumentar el tamaño del test set.
d) Aumentar el tamaño del validation set.
e) Reducir el número de capas de la red.
f) Data augmentation.

#### Cuestión 8: Supongamos que queremos entrenar una red para un problema de clasificación de imágenes con las siguientes clases: {'perro','gato','persona'}. ¿Cuántas neuronas y que función de activación debería tener la capa de salida? ¿Qué función de pérdida (loss function) debería usarse?

## Actividad 2: Redes Convolucionales
Vamos a usar el dataset cifar-10, que son 60000 imágenes de 32x32 a color con 10 clases diferentes. Para realizar mejor la práctica puede consultar [Introduction_to_CNN.ipynb](https://github.com/ezponda/intro_deep_learning/blob/main/class/CNN/Introduction_to_CNN.ipynb)

![image](https://github.com/user-attachments/assets/fe4ca745-ed82-41dd-8787-fd489ea8f599)

#### Cuestión 1: Cree una red convolucional con la API funcional con al menos dos capas convolucionales y al menos dos capas de pooling. Debe obtener un Test accuracy > 0.68
#### Cuestión 2: Cree el mismo modelo de manera secuencial. No es necesario compilar ni entrenar el modelo
#### Cuestión 3: Si tenenemos una una imagen de entrada de 300 x 300 a color (RGB) y queremos usar una red densa. Si la primera capa oculta tiene 100 neuronas, ¿Cuántos parámetros tendrá esa capa (sin incluir el bias) ?
#### Cuestión 4 Ponga las verdaderas ventajas de las redes convolucionales respecto a las densas
a) Reducen el número total de parámetros, reduciendo así el overfitting.

b) Permiten utilizar una misma 'función' en varias localizaciones de la imagen de entrada, en lugar de aprender una función diferente para cada pixel.

c) Permiten el uso del transfer learning.

d) Generalmente son menos profundas, lo que facilita su entrenamiento.

#### Cuestión 5: Para el procesamiento de series temporales las redes convolucionales no son efectivas, habrá que usar redes recurrentes.

Puedes encontrar las soluciones en el .ipynb
