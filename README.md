# ALGORTIMOS-INTELIGENCIA-ARTIFICIAL
## Introducción
Este proyecto combina conceptos de inteligencia artificial y teoría de juegos, usando Python para simular:
1.Algoritmos de búsqueda: A*
2.Heurísticas: Distancia Manhattan y Euclidiana
3.Teoría de juegos: Dilema del prisionero, Stag Hunt y coordinación de colores

El objetivo es entender cómo los algoritmos de IA y las heurísticas ayudan a tomar decisiones y cómo la teoría de juegos modela estrategias entre jugadores.

# Implementación del Algoritmo A* en Python
### Descripción del proyecto

Este proyecto implementa el algoritmo de búsqueda informada A*  utilizando el lenguaje de programación Python.
El objetivo del programa es encontrar el camino más corto entre un nodo inicial y un nodo objetivo dentro de un grafo, utilizando una función heurística que permite optimizar la búsqueda.

Además de calcular la ruta óptima, el programa incluye una visualización del grafo donde se muestra el camino encontrado resaltado.

## Algoritmo utilizado
El algoritmo implementado es A*, el cual combina:

g(n): costo real desde el nodo inicial hasta el nodo actual.
h(n): estimación heurística del costo desde el nodo actual hasta el objetivo.
f(n) = g(n) + h(n): función de evaluación utilizada para decidir qué nodo explorar.

## Este algoritmo es ampliamente utilizado en áreas como:
Inteligencia Artificial
Sistemas de navegación
Videojuegos
Robótica

## Tecnologías utilizadas

- Python
- NetworkX
- Matplotlib
- Google Colab

### Estructura del código
El programa se divide en las siguientes partes principales:

## Definición del grafo
Se representa mediante un diccionario donde cada nodo tiene sus vecinos y el costo de las conexiones.

1.Definición de la heurística
Se establece una estimación del costo desde cada nodo hasta el nodo objetivo.

2.Implementación del algoritmo A*
Se utiliza una cola de prioridad para seleccionar el nodo con menor valor de evaluación.

3.Reconstrucción del camino óptimo
Una vez encontrado el objetivo, se reconstruye la ruta desde el nodo inicial.

3.Visualización del grafo
Se genera una gráfica donde se muestra el grafo completo y el camino óptimo resaltado.

## Ejemplo de ejecución

Al ejecutar el programa se obtiene una salida similar a la siguiente:

Nodo visitado: X
Nodo visitado: Z
Nodo visitado: M
Nodo visitado: I

Ruta encontrada: ['X', 'Z', 'M', 'I']
Costo total: 5

Esto indica que el algoritmo encontró que la ruta más corta desde el nodo X hasta el nodo I es pasando por Z y M, con un costo total de 5.

Además, se muestra una visualización del grafo, donde el camino óptimo aparece resaltado en color rojo.

## Conclusión

La implementación del algoritmo A* permite encontrar de manera eficiente el camino más corto entre dos nodos en un grafo utilizando información heurística.

Este proyecto demuestra cómo los algoritmos de búsqueda informada pueden optimizar la exploración de estados, reduciendo el número de nodos evaluados en comparación con métodos de búsqueda no informados.

La visualización del grafo facilita la comprensión del proceso y permite identificar claramente el camino óptimo encontrado por el algoritmo.

#### Ejemplos de Heurísticas en Inteligencia Artificial

## Descripción
Este proyecto presenta dos ejemplos básicos de funciones heurísticas utilizadas en algoritmos de búsqueda informada en Inteligencia Artificial. Las heurísticas permiten estimar la distancia o costo desde un estado actual hasta el objetivo, ayudando a los algoritmos a encontrar soluciones de manera más eficiente.

En este caso se implementan dos heurísticas comunes para calcular distancias entre puntos en un plano:

Distancia Manhattan
Distancia Euclidiana

Ambas se utilizan frecuentemente en algoritmos de búsqueda como A*.

## Tecnologías utilizadas
El proyecto fue desarrollado utilizando:

Python
Python math module para cálculos matemáticos

Heurística 1: Distancia Manhattan

La distancia Manhattan calcula la distancia entre dos puntos sumando las diferencias absolutas de sus coordenadas en los ejes X y Y.
​
## características

Se utiliza en entornos de cuadrícula.
Representa movimientos solo horizontales y verticales.
Es común en videojuegos, mapas y robótica.

## Ejemplo de salida
La distancia Manhattan entre (2, 3) y (7, 8) es: 10

## Heurística 2: Distancia Euclidiana

La distancia Euclidiana calcula la distancia directa entre dos puntos en un plano cartesiano, representando la línea recta más corta entre ellos

## Características

Representa la distancia real en línea recta.
Permite movimientos en cualquier dirección.
Es muy utilizada en sistemas de navegación y geometría computacional.

## Ejemplo de salida
La distancia Euclidiana entre (1, 2) y (6, 7) es: 7.07

## Estructura del código
El proyecto incluye dos programas principales:

## Función heurística Manhattan
Recibe dos puntos como tuplas.
Calcula la distancia usando diferencias absolutas.

## Función heurística Euclidiana
Recibe dos puntos como tuplas.
Calcula la distancia utilizando la función math.hypot().

## Conclusión
Las heurísticas son herramientas fundamentales en la Inteligencia Artificial, ya que permiten estimar el costo de llegar a un objetivo y mejorar la eficiencia de los algoritmos de búsqueda. En este proyecto se implementaron dos de las heurísticas más comunes: la distancia Manhattan y la distancia Euclidiana. Cada una es útil dependiendo del tipo de problema y del tipo de movimiento permitido en el en

## TEORIA DE JUEGOS 

## Introducción
La teoría de juegos es una rama de las matemáticas que analiza cómo los individuos o agentes toman decisiones estratégicas cuando el resultado de sus acciones depende de las decisiones de los demás. Esta disciplina permite comprender y predecir comportamientos en situaciones de interacción, competencia o cooperación entre diferentes participantes.

Se utiliza en diferentes áreas como:

economía
Inteligencia artificial
Biología
Ciencias políticas
Informática

En este proyecto se presentan tres ejemplos simples de teoría de juegos implementados en Python, donde se simulan decisiones entre jugadores y se observan los resultados según las estrategias elegidas.

## Ejemplo 1 – Dilema del prisionero

El Prisoneros  Dilemma es uno de los ejemplos más conocidos de la teoría de juegos.
En este problema dos jugadores deben elegir entre:

Cooperar (C)
Traicionar (T)
Dependiendo de sus decisiones, reciben diferentes recompensas.

## funcionamiento del programa

El código simula el juego de la siguiente manera:
Se definen dos estrategias posibles: cooperar o traicionar.
Cada jugador selecciona una estrategia de forma aleatoria.
Se utiliza una matriz de pagos representada con un diccionario.
El programa muestra las elecciones de los jugadores y el resultado obtenido.

Ejemplo de salida
Jugador 1: C
Jugador 2: T
Resultado: Jugador 2 traiciona → gana 5 puntos
Ejemplo 2 – Juego de coordinación (Stag Hunt)

El Stag Hunt o juego de caza del ciervo es un modelo de coordinación donde los jugadores pueden cooperar para obtener una mayor recompensa o elegir una opción segura con menor beneficio.

En este ejemplo los jugadores pueden elegir entre:
Cazar Ciervo (C) → mayor recompensa si ambos cooperan
Cazar Conejo (R) → recompensa menor pero segura

## Funcionamiento del programa

El programa realiza lo siguiente:
Simula varias rondas del juego.
Cada jugador elige una estrategia de forma aleatoria.
Se asignan puntos según las decisiones de ambos jugadores.
Se acumulan los puntajes de cada ronda.
Se genera un gráfico con la evolución de los puntajes usando Matplotlib.

## Ejemplo de salida
Ronda 1
Jugador 1 eligió: C
Jugador 2 eligió: R
Resultado: Jugador 1 pierde la oportunidad → Jugador 2 gana 2 puntos

El programa también muestra un gráfico de la evolución de los puntajes durante las rondas.

## Ejemplo 3 – Juego de coordinación de colores

Este ejemplo representa un juego de coordinación simple, donde dos jugadores deben elegir el mismo color para obtener una recompensa.

Los jugadores pueden elegir entre:

Rojo (R)
Azul (A)

## Funcionamiento del programa

El programa ejecuta varias rondas del juego:

Cada jugador selecciona un color aleatoriamente.
Si ambos jugadores eligen el mismo color, obtienen puntos.
Si eligen colores diferentes, no reciben puntos.
Se acumulan los puntajes de cada jugador.

Al final se muestra el ganador o si hubo empate.

## Ejemplo de salida
Ronda 1
Jugador 1 eligió: R
Jugador 2 eligió: R
Resultado: ¡Coordinación lograda! → 3 puntos cada uno

## Conclusión

Este proyecto demuestra cómo la Inteligencia Artificial y la Teoría de Juegos pueden combinarse para:
Optimizar la toma de decisiones con algoritmos informados
Simular estrategias y resultados entre jugadores
Visualizar de manera clara caminos óptimos y resultados de juegos
Estos modelos son útiles en economía, robótica, sistemas de navegación y toma de decisiones estratégicas.


## Autor
Kelly Mosquera  
Estudiante de Ingeniería de Sistemas
