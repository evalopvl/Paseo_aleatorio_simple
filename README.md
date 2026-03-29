# Paseo_aleatorio_simple
Este repositorio contiene una simulación del Paseo Aleatorio Simple (PAS) junto con su análisis teórico y visualización mediante Python.

El Paseo Aleatorio Simple es un proceso estocástico definido en $T = \{1, 2, ...\} = \mathbb{N}$, que toma valores en  $S = \mathbb{Z}$.

Para cada $t \in \mathbb{N}$, el proceso se define como $$X_t = \sum_{s=1}^{t} Z_s$$ siendo $\{Z_s\}_{s \in \mathbb{N}}$ variables aleatorias independientes e idénticamente distribuidas (i.i.d.) según la siguiente distribución: $$P(Z_s = 1) = p, \quad P(Z_s = -1) = 1-p$$

Se puede calcular la media teórica $E[X_n]$ de forma cerrada: $$E[X_n] = E[\sum_{i=1}^{n} Z_i] = \sum_{i=1}^{n}E[Z_i] = (2p-1)n$$

Por otra parte, la varianza teórica se calcula como sigue: $$Var(X_n) = \sum_{i=1}^{n}Var(Z_i) = 4p(1-p)n$$

Para calcular la desviación típica es suficiente con hacer la raíz cuadrada de la varianza: $\sigma(X_n) = \sqrt{Var(X_n)}$

El objetivo de este proyecto es implementar una simulación de este proceso y analizar cómo el parámetro $p$ influye en el comportamiento de las trayectorias.

## Visualizaciones
En este proyecto se realizan tres tipos de visualizaciones principales del Paseo Aleatorio Simple:

### Trayectorias del proceso
Se representan varias trayectorias simuladas del PAS, para distintos valores del parámetro $p$.

### Trayectorias con media y desviación teórica
Se superponen las trayectorias simuladas con:

* la media teórica del proceso
* bandas correspondientes a la desviación típica

Esto permite visualizar cómo se distribuyen las trayectorias alrededor de la media y cómo crece la variabilidad con el tiempo.

### Media empírica al aumentar el número de trayectorias
Se estudia la evolución de la media empírica del proceso al aumentar el número de trayectorias consideradas.

## Tecnologías empleadas
Se ha hecho uso del lenguaje de programación python en el entorno de Google Colab, y las siguientes librerías
* numpy
* matplotlib
