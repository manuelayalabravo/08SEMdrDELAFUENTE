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


Profesor Sr. Sebastián Cea corrige error del codigo para insertar análisis de bibliografía desde la Web of Science. corregido

se corrige ingreso de cite style languaje csl. corregido ingresando el código:

output: 
  pdf_document: 
    keep_tex: yes
    latex_engine: xelatex  
    citation_package: biblatex
    
Queda funcionando archivo +.Rmd. se termina edición de informe tipo referee del seminario Dr. De La Fuente.

se consideran las siguientes competencias adquiridas
redacción en rmarkdown
redacción en LaTex overleaf 
inclusión de referencias +.bib
utilización de Zotero
estilo de citas csl
inclusión de diagramas TIKZ
utilización de CITR
utilización de Web of Science
extracción de datos desde la Web of Science en plaintext y BibTex
uso de bibliometrix web
uso de bibliometrix en archivo *.Rmd
escritura de formulas en LaTex

