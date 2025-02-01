---
title: "Obteniendo datos de archivos CSV"
slide_level: 1
fontsize: 9pt
---

# Archivos

## Definición
Un archivo es una manera de guardar información en una computadora.
De manera general se distiguen dos tipos de archivos: archivos de texto y archivos binarios.

## Archivos de texto
Archivos almacenados de acuerdo a una codificación de texto.

## Archivos binarios
Todos los demás, es decir los archivos que no tienen una codificación de texto.

# Abriendo archivos

## open 

    open(filename, mode, encoding=None)

- filename: nombre del archivo, por ejemplo: datos.csv, 2023_04.dat, enero.txt, etc.
- mode: modo de apertura. Existen 3 modos: lectura, escritura y agregar ('r', 'w' y 'a' respectivamente).
- encoding: el tipo de codificación que se debe usar, lo más común es "utf-8" pero en Windows se suele usar "Latin1".

\*Se puede ver la lista completa de codificaciones [aquí](https://docs.python.org/3/library/codecs.html#standard-encodings)

## close
Una vez abierto y realizadas las operaciones necesarias con el archivo, es necesario cerrarlo para evitar pérdida de información. Esto se realiza con el método `close()`.

# Ejemplo:

## 

    f = open('workfile', 'r', encoding="utf-8")
    # leer datos...
    f.close()

# Archivos CSV

::: {.block}
## Definición
Son archivos de **texto** datos tabulares, con columnas separadas por **comas**, o algún otro caracter de separación (un espacio, por ejemplo).
:::
- Suelen tener una zona de encabezado al inicio del archivo.
- Su estructura es simple
- Son fáciles de leer y escribir
- Tienen un uso muy difundido, por lo que muchos programas los pueden leer, escribir y procesar.
- Típicamenta la primer o primeras columnas se utilizan para almacenar fecha y hora.

\center
\includegraphics[width=0.7\textwidth]{img/csv_file.png}


# Obteniendo valores de un archivo CSV
Existen diferentes bibliotecas con las que se puede acceder a los archivos CSV en Python.
Sin embargo, al ser archivos muy simples, el acceso se puede hacer con una rutina propia.
El siguiente script nos permite extraer los datos en la columna 4, de un archivo separado por comas y codificado en "LATIN1".
Los datos quedan almacenados en la lista denominada **datos**

\center
\includegraphics[width=0.7\textwidth]{img/csv_getC.png}

# Graficando CSV
La biblioteca más popular para graficar en Python es matplotlib ([matblotlib.org](https://matplotlib.org/))
- Tiene una documentación extensa

\center
\includegraphics[width=0.7\textwidth]{img/matplotlib.png}
