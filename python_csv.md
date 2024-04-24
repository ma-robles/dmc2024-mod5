---
title: "Obteniendo datos de archivos CSV"
slide_level: 1
fontsize: 9pt
---

# Abriendo archivos

## open 

    open(filename, mode, encoding=None)

- filename: nombre del archivo, por ejemplo: datos.csv, 2023_04.dat, enero.txt, etc
- mode: modo de apertura. Existen 3 modos: lectura, escritura y agregar ('r', 'w' y 'a' respectivamente)
- encoding: el tipo de codificación que se debe usar, lo más común es "utf-8" pero en Windows se suele usar "Latin1"

\*Se puede ver la lista completa de codificaciones [aquí](https://docs.python.org/3/library/codecs.html#standard-encodings)

## close
Una vez abierto y realizadas las operaciones necesarias con el archivo, es necesario cerrarlo para evitar pérdida de información. Esto se realiza con el método `close()`.

# Ejemplo:

## 

    f = open('workfile', 'r', encoding="utf-8")
    # leer datos...
    f.close()

# Archivos

## Definición
x

## Archivos de texto
x

## Archivos binarios
x

# Archivos CSV

## Definición
Son archivos de datos tabulares, con columnas separadas por comas


# Obteniendo valores de un archivo CSV
xxx

# Graficando CSV
xxx


