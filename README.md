# 08SEMdrDELAFUENTE
Seminario Dr. De la Fuente. Fecha01jul2920
la inteción de este comentario es iniciarme en la metodología de trabajo con control de cambio GitHub..
Se inicia proyecto de control de flujo Kanban Done
No se encontró artículo 1, sobre estudio de municipalidades y eficiencia, artículo 1 Done
se realiza prueba de Tikz, funciona codigo pero cambia el font del texto original y cambia la posición del texto.
Se actualiza paquete bibliometrix a su última versión
se ingresa a la carpeta del proyecto base de datos de busqueda bibliográfica de la WebOfScience. en formatos .bib y plaintext savedrecs-3.bib savedrecsDLF.txt
codigo de lectura de biblioetrix desde r markdown no funciona


#bibliometrix

```{r message=FALSE, warning=FALSE, include=FALSE}
library(bibliometrix)   
file <- "https://www.bibliometrix.org/datasets/savedrecsDLF.txt"
M <- convert2df(file, dbsource = "wos", format = "plaintext")
head(M["TC"])
results <- biblioAnalysis(M, sep = ";")
```

```{r message=FALSE, warning=FALSE}
plot(x = results, k = 10, pause = FALSE)
```

```{r}
topAU <- authorProdOverTime(M, k = 10, graph = TRUE)
```
archivo de trabajo: RefereeSEM_DeLaFUENTE.Rmd
