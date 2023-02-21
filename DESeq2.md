# Rnaseqpinaster #
## Análisis diferencial DESeq2 ##
### Pruebas Biorender ###

Vamos a realizar un anális DESeq2. Primero cargaremos los datos o los leeremos. Tenemos que instalar varias librerías

install.packages()

library("tximport")
library("readr")
library("DESeq2")
library("ggplot2")

#### PRIMERO CARGAMOS LOS DATOS ####

Con el siguiente código establezco mi *working directory*. Compruebo que esté bien establecido con getwd(). Con outputPrefix le digo que los archivos acaben en esa terminación.

`outputPrefix <- "raizpinaster_deseq2"`

`dir <- "/Users/trast/Documents/Universidad/Máster/TFM-INIA-P/Counts/Counts"`

`setwd(dir)`

`getwd()`

Lo siguiente es crear un vector que llamaremos *filenames* que contenga los nombres de los outputs obtenidos después de usar Kallisto. full.names= TRUE es para que coja todo el nombre del archivo, pattern="* quant.sf" es todo lo que acabe en quant.sf y que antes haya cualquier carácter. 

`filenames <- list.files(pattern="*quant.sf", full.names=TRUE)`

Comprobamos que se haya realizado bien con las funciones
```
length(filenames)
str(filenames)
filenames
  ```
