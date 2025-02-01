---
title: "Archivos netCDF"
slide_level: 1
fontsize: 9pt
---

# Archivos NetCDF (Network Common Data Form) 
A diferencia de los archivos CSV, que están pensados básicamente para almacenar series de tiempo, 
los NetCDFs están pensados para compartir de manera eficiente datos científicos estructurados en arreglos (multidimensionales).

- Autodescriptivo
- Portable a diferentes sistemas
- Se le pueden agregar datos sin necesidad de modificar la estructura original
- Se puede leer de manera simultánea (por varios lectores)
- Existen diversas herramientas y bibliotecas de diferentes lenguajes gratuitas que se pueden usar


# NetCDF en Python

En python se puede utilizar la biblioteca netCDF4 para leer, crear y modificar netCDF. 
Puede consultarse la documentación en [https://unidata.github.io/netcdf4-python/](https://unidata.github.io/netcdf4-python/)


\center
\includegraphics[width=0.7\textwidth]{img/netcdf4.png}

# Instalación
Se puede instalar desde pip o desde anaconda(si es que no la tenemos instalada aun):

- pip install netCDF4
- conda install -c conda-forge netCDF4

# Scripts de ejemplo

Descargue los scripts de ejemplo de la siguiente página de github:
[https://github.com/ma-robles/ex_netcdf](https://github.com/ma-robles/ex_netcdf)

- Sino sabe usar github, una vez ingresado en la página, de click en el botón azul que dice _Code_, ahí seleccione _Download ZIP_
- Se realizará la descarga de los scripts en una carpeta comprimida, bastará descomprimir

Si se encuentra en la plataforma web del diplomado, puede descargarlo con la instrucción:

```
git clone https://github.com/ma-robles/ex_netcdf.git
```

- En este segundo caso, se creará de manera automática una carpeta llamada _ex_netcdf_ con los archivos de ejemplo

# Lectura
El script read_data_nc.py nos permite ver diferentes parámetros de un archivo netCDF.
Para ejecutarlo debemos agregar el nombre del archivo netCDF que deseamos abrir después del nombre de nuestro script, algo como:
```
python read_data_nc.py archivo.nc
```
Donde:

- read_data_nc.py es el nombre del script
- archivo.nc es la ruta y nombre del archivo netCDF que deseamos abrir

Es recomendable copiar el archivo netCDF a la carpeta donde ejecutamos el script de Python (read_data_nc.py)

# Lectura (continuación)
A continuación vemos un ejemplo de la salida obtenida.
Podemos observar el nombre del archivo, la versión del netCDf, las diferentes dimensiones de las variables que existen y,
finalmente un diccionario con los nombres de las variables.

\center
\includegraphics[width=0.95\textwidth]{img/netcdf_read.png}

# Graficado

Una de las herramientas básicas que podemos usar para graficar es _cartopy_ ( en combinación con matplotlib).
La página con la documentación, la podemos encontrar en 
[https://scitools.org.uk/cartopy/docs/latest/](https://scitools.org.uk/cartopy/docs/latest/)

y la podemos instalar en conda con la siguiente instrucción (en el anaconda promt)
```
conda install conda-forge::cartopy
```


\center
\includegraphics[width=0.5\textwidth]{img/cartopy.png}

# Graficando temperatura

El script _plot_data_nc.py_ se corre de la misma manera que los scripts anteriores (agregando el nombre del archivo netCDF).
Sin embargo, ahora realiza la lectura del netCDF, extrae los valores de la variable _T2_ (temperatura del aire a 2m), realiza una gráfica y la almacena como *figure_nc.png*.

- Se limita la graficación a la latitud y longitud máxima y mínima,
- se indica dibujar un grid con etiquetas arriba y a la derecha.
- también dibujar las líneas de costa.

El resultado se observa a continuación:

\center
\includegraphics[width=0.5\textwidth]{img/figure_nc_temp.png}

# Ejercicio

##

Modifique el script _plot_data_nc.py_ de manera que obtenga las variables RAINC y RAINNC, en el tiempo que desee.
Observe que existe 121 "tiempos", lo que representa un dato por hora.
Además modifique el título que dice "variable" en la parte inferior (con el texto que mejor le parezca).


# Agregando archivos Shape

Es posible agregar archivos shape para enriquecer nuestra gŕafica.
Podemos descargar archivos shape, con diferente tipo de información y resolución de la página: 
[https://www.naturalearthdata.com/](https://www.naturalearthdata.com/)

cartopy nos permite descargar estos archivos de manera automática de la página mencionada,
pero también podemos agregar archivos shape que tengamos almacenados localmente.

El script plot_data_shp_nc.py agrega los limites de los países de manera automática y los límites de los estados de un shapefile almacenado localmente (aunque extraido de la misma página).
El archivo, nuevamente, se guarda como archivo .PNG.

\* Los límites de los países no se notan debido a la zona de trabajo limitada.
\* Antes de correr el script verifique que la ruta indicada para el archivo shape (shp) coincide con la ruta donde lo colocó. Originalmente el script indica que se encuentra en /tmp/shp/

# Gráfica shape
A continuación se muestra el resultado

\center
\includegraphics[width=0.85\textwidth]{img/figure_nc_shp.png}

# Otros...

Los demás scripts de ejemplo realizan graficación de viento de manera similar a la ya realizada,
sin embargo es posible que obtenga un error al correr, dado que hay una diferencia con los nombres y dimensiones de las variables **lat** y **lon**.
Deben modificarse a LAT y LONG respectivamente, así como agregar la dimensión tiempo.
Dichas modificaciones si se realizaron en los scripts descritos anteriormente.

A manera de ejercicio (no obligatorio) intente realizar las modificaciones necesarias para correr estos scripts

