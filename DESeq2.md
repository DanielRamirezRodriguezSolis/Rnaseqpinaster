# Rnaseqpinaster
## Análisis diferencial DESeq2 ##
### Pruebas Biorender ###

Vamos a realizar un anális DESeq2. Primero cargaremos los datos o los leeremos. Tenemos que instalar varias librerías

install.packages()

library("tximport")
library("readr")
library("DESeq2")
library("ggplot2")

# PRIMERO CARGAMOS LOS DATOS # 

Con el siguiente código establezco mi *working directory*. Compruebo que esté bien establecido con getwd(). Con outputPrefix le digo que los archivos acaben en esa terminación.

`outputPrefix <- "raizpinaster_deseq2"`

`dir <- "/Users/trast/Documents/Universidad/Máster/TFM-INIA-P/Counts/Counts"`

`setwd(dir)`

`getwd()`
