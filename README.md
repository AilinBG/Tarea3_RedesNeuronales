# Tarea 3: Funciones, Modelos personalizados y Ecuaciones Diferenciales

Este repositorio contiene la implementación de la Tarea 3 de la materia de Redes Neuronales utilizando Python, TensorFlow y Keras.

## Contenido

### Problema 1. Capa personalizada para escala de grises

Se diseñó una capa personalizada de Keras que transforma imágenes a color RGB en imágenes de escala de grises.

La capa no contiene parámetros entrenables, por lo que no requiere entrenamiento.

### Problema 2. Aproximación de funciones mediante redes neuronales

Se entrenaron redes neuronales para aproximar las siguientes funciones en el intervalo [-1, 1]:

#### 2(a)

$$
f(x)=3\sin(\pi x)
$$

A partir de estos datos se entrenó una red neuronal densa para aprender la relación no lineal entre (x) y (y).
El ejercicio permite observar cómo una red neuronal puede aproximar una función matemática sin proporcionarle explícitamente su expresión durante el entrenamiento.

#### 2(b)
Para este ejercicio se generaron 2000 valores de entrada en el intervalo ([-1,1]). Los valores de salida se obtuvieron mediante la función:

$$
f(x)=1+2x+4x^3
$$
La función utilizada combina términos constante, lineal y cúbico, por lo que presenta un comportamiento no lineal.
Se entrenó una red neuronal densa para aproximar esta relación a partir de los datos generados.
Durante las primeras pruebas se obtuvo una pérdida elevada, por lo que se revisó la implementación y se corrigió la generación de los valores de salida. Después de la corrección, el modelo logró aproximarse adecuadamente a la función objetivo.

Para cada función se muestra la comparación entre la función original y la aproximación obtenida por la red neuronal, así como la métrica RMSE.

### Problema 3. Capa entrenable

En este ejercicio se utilizó una estructura cuyos parámetros permiten representar una función de la forma:
$$
f(x) = a_0 + a_1x + a_2x^2 + a_3x^3
$$ 
El objetivo es ajustar los parámetros del modelo para aproximar la función:
$$
y = \cos(2x)
$$
A diferencia de los ejercicios anteriores, aquí la estructura del modelo está relacionada directamente con un polinomio de tercer grado.
El entrenamiento permite observar cómo los parámetros se modifican para minimizar la diferencia entre los valores predichos y los valores reales.

### Problema 4. Ecuaciones diferenciales

Se utilizaron redes neuronales para aproximar las soluciones de ecuaciones diferenciales ordinarias.

#### 4(a)
Se trabajó con la ecuación diferencial:
$$
xy'+y=x^2\cos(x)
$$

con la condición inicial:
$$
y(0)=0
$$

El objetivo es utilizar una red neuronal para obtener una aproximación de la solución de la ecuación diferencial, incorporando tanto la ecuación como la condición inicial en el proceso de entrenamiento.
Este ejercicio permite observar una aplicación diferente de las redes neuronales, en la que el objetivo no es únicamente aprender a partir de pares de datos, sino utilizar información matemática del problema para aproximar su solución.

#### 4(b)
En el segundo problema se continuó con la aplicación de redes neuronales para aproximar la solución de la ecuación diferencial.
$$
y''=-y, \qquad y(0)=1,\qquad y'(0)=-0.5
$$
Se construyó el modelo considerando la ecuación diferencial correspondiente y las condiciones necesarias para obtener una solución consistente.
El entrenamiento busca minimizar el error asociado al cumplimiento de la ecuación, permitiendo que la red neuronal encuentre una función que se aproxime a la solución buscada.

Para ambos casos se compara la solución obtenida mediante la red neuronal con la solución analítica y se reportan los errores correspondientes.

## Resultados
Los ejercicios permitieron comprobar que una red neuronal puede utilizarse para aproximar diferentes tipos de relaciones matemáticas.
En particular, los ejercicios de aproximación de funciones mostraron que:
Las redes neuronales pueden aprender relaciones no lineales.
La elección de la arquitectura y los hiperparámetros influye en el proceso de entrenamiento.
La función de pérdida permite evaluar qué tan cerca se encuentran las predicciones del modelo respecto a los valores objetivo.
La generación y preparación correcta de los datos es fundamental para obtener un entrenamiento adecuado.
En el ejercicio de la función cúbica fue necesario revisar la implementación debido a que inicialmente se obtuvo un valor de pérdida elevado. Después de corregir la generación de los datos, se obtuvo un comportamiento adecuado del entrenamiento.
Los ejercicios de ecuaciones diferenciales permitieron extender el uso de redes neuronales hacia problemas donde se busca aproximar una función que satisfaga determinadas restricciones matemáticas.

## Organización del repositorio

Todos los problemas e incisos se encuentran en la rama `main`.

El desarrollo de la tarea y sus modificaciones se encuentran registrados en el historial de commits del repositorio.

## Archivo principal

`Tarea3_Funciones_Modelos_EDO.ipynb`
