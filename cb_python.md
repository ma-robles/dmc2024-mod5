---
title: "Conceptos Básicos de Python"
slide_level: 1
fontsize: 9pt
---

# Qué es python

## Python
Es un lenguaje de programación de **alto nivel**, **interpretado** y **orientado a objetos** que hace énfasis en la legibilidad de su código.

# Porqué usar Python

- Es gratis
- Es de código abierto
- Tiene un amplio rango de aplicaciones
- Es sencillo de usar
- Es multiplataforma
- Hay una gran comunidad activa

# Descarga e instalación

::: columns

:::: column
- Página oficial ([python.org](python.org/downloads/))
- Chocolatey (en Windows)

    choco install python

::::

:::: column
Administradores de paquetes

- PIP (pre-instalado)

- [Anaconda](https://www.anaconda.com/download/success)

::::

:::

# Modos de Operación

::: columns

:::: column
## Intérprete
Permite el envío de instrucciones de manera individual, la respuesta es "inmediata".

- Es útil para probar sintáxis o fragmentos de código

::::

:::: column

## Script
Ejecuta un programa almacenado en un archivo.

- Forma de uso más común y más recomendada

::::

:::

# Modo Intérprete

1. Ingrese a su emulador de terminal (*Anaconda Prompt* en su computadora  o *Terminal* en [Tlaloc](https://tlaloc.atmosfera.unam.mx:9000/hub/login). 
    - Al ingresar observará una ventana con texto finalizando con **$**. 
    - El texto suele hacer referencia a su nombre de usuario y nombre del equipo.

\center
\includegraphics[height=0.6\textheight]{img/tlaloc_terminal.png}
\includegraphics[height=0.6\textheight]{img/tlaloc_terminal_in.png}

# Modo Intérprete

2. Escriba python \keys{\return}
    - Observará info de la versión de Python y un *prompt* conformado por 3 símbolos "*>*".
    - El *prompt* nos indica que el intérprete está listo para recibir órdenes

\center
\includegraphics[height=0.8\textheight]{img/python_ini.png}

# Hola mundo

3. Ejecute

    print("Hola mundo") \keys{\return}
    - *print* es la instrucción para mostrar mensajes
    - El interprete mostrará el mensaje indicado

\center
\includegraphics[height=0.7\textheight]{img/hola.png}

# Variables

## Una variable es una (o más) localidades de memoria que pueden tomar algún valor
- Se les asigna un nombre al inicializarlas (darles valor por primera vez)
- No es necesario indicar su tipo
- Puede cambiar su valor o tipo en cualquier parte del programa
- Los nombres distinguen entre mayúsculas y minúsculas y deben comenzar con una letra o número
- Los nombres no pueden ser alguna palabra reservada

\center
\includegraphics[width=0.7\textwidth]{img/python_keywords.png}

# Tipos de variables

## Tipos de datos nativos básicos

| **Básicos**  | **Compuestos** |
|:---|:---|
|   `>>> flotante = 1.0` |    `>>> tupla = (10.9, 10.8, 10)` |
|  `>>> cadena = "Esto es una cadena"` | `>>> dic = { 1:'enero', 2:'febrero', 3:'marzo'}` |
|   `>>> booleano = True` | |


prueba creando las variables en la tabla

# Transformando entre tipos

## Se puede transformar de un tipo de variable a otra
-  **int(val)**: transforma a entero
-  **float(val)**: transforma a flotante
-  **str(val)**: transforma a cadena

## Ejercicio: Usando el intérprete de Python transforma

- **3.1415** a entero y a cadena
- **2** a flotante y a cadena
- **"23.12"** a flotante y a entero

# Instrucciones de decisión e iteración

\center
\includegraphics[width=0.8\textwidth]{img/python_sintax.png}


# for

## 
La instrucción *for* es especial, ya que nos facilita "recorrer" variables "iterables"; como listas, tuplas e incluso archivos.

## Ejercicio:
Crear una lista y mostrar sus elementos (uno por línea) utilizando un ciclo *for*

# Dividiendo cadenas

## Ejercicio:
Crear una variable que contenga la siguiente cadena e imprimir los valores por separado (uno por línea) utilizando un ciclo *for*

    2024-04-01 13:00:00,27.07,13.2,2.578,6.28,18.2,0.0,778.204,1000.5

## Respuesta
\center
\includegraphics[width=0.95\textwidth]{img/python_split.png}

# Abriendo archivos

# Obteniendo valores de un archivo CSV

# Graficando CSV



