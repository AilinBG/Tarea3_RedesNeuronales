# Tarea 3: Funciones, Modelos personalizados y Ecuaciones Diferenciales

Este repositorio contiene la implementación de la Tarea 3 de la materia de Redes Neuronales utilizando Python, TensorFlow y Keras.

## Contenido

### Problema 1. Capa personalizada para escala de grises

Se diseñó una capa personalizada de Keras que transforma imágenes a color RGB en imágenes de escala de grises.

La capa no contiene parámetros entrenables, por lo que no requiere entrenamiento.

### Problema 2. Aproximación de funciones

Se entrenaron redes neuronales para aproximar las siguientes funciones en el intervalo [-1, 1]:

#### 2(a)

$$
f(x)=3\sin(\pi x)
$$

#### 2(b)

$$
f(x)=1+2x+4x^3
$$

Para cada función se muestra la comparación entre la función original y la aproximación obtenida por la red neuronal, así como la métrica RMSE.

### Problema 3. Capa entrenable

Se diseñó una capa personalizada que representa el polinomio de grado 3:

$$
f(x)=a_0+a_1x+a_2x^2+a_3x^3
$$

Los coeficientes \(a_0,a_1,a_2,a_3\) son parámetros entrenables.

La capa se entrenó para aproximar:

$$
f(x)=\cos(2x)
$$

en el intervalo [-1, 1].

### Problema 4. Ecuaciones diferenciales

Se utilizaron redes neuronales para aproximar las soluciones de ecuaciones diferenciales ordinarias.

#### 4(a)

$$
xy'+y=x^2\cos(x), \qquad y(0)=0
$$

#### 4(b)

$$
y''=-y, \qquad y(0)=1,\qquad y'(0)=-0.5
$$

Para ambos casos se compara la solución obtenida mediante la red neuronal con la solución analítica y se reportan los errores correspondientes.

## Organización del repositorio

Todos los problemas e incisos se encuentran en la rama `main`.

El desarrollo de la tarea y sus modificaciones se encuentran registrados en el historial de commits del repositorio.

## Archivo principal

`Tarea3_Funciones_Modelos_EDO.ipynb`
