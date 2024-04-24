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

# Ejercicios de variables

## Ejercicio "Hola variable"
Repite el programa _"Hola mundo"_ utilizando una variable, escribe las siguientes líneas en el intérprete de Python:

    >>> saludo = "hola mundo"
    >>> print(saludo)

## Ejercicio
Prueba creando las variables de la tabla en el intérprete de Python. Para ver el valor de una variable en el intérprete, basta con escribir su nombre + \keys{\return} o con ayuda de la función `print`

# Transformando entre tipos

## Se puede transformar de un tipo del valor de una variable a otro
- **int(val)**: transforma a entero
- **float(val)**: transforma a flotante
- **str(val)**: transforma a cadena
- **type(var)**: indica el tipo de variable

_val_ es una variable de un tipo diferente al deseado

## Ejemplo:
Convertir la variable n= 2.0 a entero:

    >>>n=2.0
    >>>int(n)
    2
Se puede observar que _int_ devuelve un entero (2)

## Ejercicio: Usando el intérprete de Python verifica el tipo inicial y transforma al tipo que se indica.

- **3.1415** a entero y a cadena
- **2** a flotante y a cadena
- **"23.12"** a flotante y a entero

# Instrucciones imperativas 

## Instrucciones básicas
- print
- input
- conversiones de tipos
- operaciones matemáticas 
- comparaciones 

# print

## Descripción:
Imprime una o más variables en una línea, si son más de una variable, se usa un carácter de separación. El carácter de separación por defecto es un espacio. También existe un carácter de fin de línea, por defecto es el carácter \\n o "nueva línea". Por defecto imprime en la pantalla pero puede imprimir en un archivo.

## Sintaxis básica 
print ( <variable 1>, <variable 2>, ...)

## Personalizando
print( < variable(s) >, sep=<caracter de separación>, end=<caracter de fin de línea>)

# input

## Descripción:
Obtiene valores del usuario y los regresa como una cadena de texto que se puede almacenar en una variable

## Sintaxis
```
<respuesta> = input(<mensaje>)
```

## Ejemplo
\center
\includegraphics[width=0.5\textwidth]{img/python_input.png}


# Operaciones matemáticas, lógicas y comparaciones
Estas operaciones son bastante simples y "estandar". Consultar cheatsheet adjunta.

Como ejercicio, pruebe realizar algunas en el intérprete

# Modo Script 

## Ejecución 
- Se escribe *Python* + espacio + archivo
*archivo* es el nombre del archivo donde se encuentran las instrucciones. Típicamente tiene terminación .py

## Algoritmo para crear y correr un script
- Crear archivo con instrucciones de python.
- Guardar el archivo con terminación.py
- Abrir terminal con acceso a Python
- Cambiarse al directorio donde se encuentra nuestro archivo .py
- Ejecutar escribiendo python + archivo

# Ejercicios Script

## hola mundo con nombre
Crear un script que pregunte el nombre del usuario, reciba el nombre y responda con "Hola"+nombre

## par o impar
Crear y correr un script que verifique si el valor ingresado es par o impar. También valide que el número sea entero, de lo contrario muestre un mensaje indicando el error.


# Instrucciones de decisión e iteración

##
Este tipo de instrucciones requieren de un bloque de código que se realiza cuando se cumple alguna condición. En Python, para delimitar un bloque de código se utiliza un _"sangrado"_, es decir, cierto espacio inicial, con el cual se encuentra alineado todo el bloque.
Por esto, en Python, es de suma importancia el espaciado inicial que se le da cada línea de código. De manera etándar se utiliza un sangrado de 4 espacios.

## Sintaxis
Su sintaxis consiste de las palabras if/while seguidas de la condición a evaluar y terminando por _":"_ (dos puntos).
Las instrucciones siguientes se deben _sangrar_ para indicar que pertenecen al bloque.
Para finalizar el bloque, simplemente se deja de sangrar.

# Ejemplos

## Ejemplo if:
\center
\includegraphics[width=0.8\textwidth]{img/python_if.png}

## Ejemplo while:
\center
\includegraphics[width=0.8\textwidth]{img/python_while.png}



# Resumen de instrucciones de decisión e iteración

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

