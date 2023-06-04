---
title: "Introducción a Phyloseq"
date: "2023-05-24T21:48:51-07:00"
tags: ["Bioconductor", "Phyloseq", "Metagenomics"]
output: html_document
bibliography: phyloseq.bib
link-citations: true
---

<style>
#TOC {

  color: #99A7DE;
  background-color: #F5F5F5;

}
#header {
  
  text-align: center;
  color: #A36DD0;
  background-color: #F5F5F5;
  opacity: 0.8;
  font-family: serif;
  
}
h1, h2, h3, h4 {
  
  color: #99A7DE;
  opacity: 0.8;

}
body {

    font-family: cambria;
    text-align:justify;
    background-color: #F5F5F5;
    
}
pre {

    font-family: Serif;
    
}
</style>

# Introducción a Phyloseq: Análisis de Microbiomas en R

## ¿Qué es Phyloseq?

**Phyloseq** es un paquete de R que se compone de una serie de funciones para importar, almacenar, analizar y visualizar gráficamente datos de secuenciación filogenética complejos que ya han sido agrupados en Unidades Taxonómicas Operativas (OTUs), especialmente cuando hay datos de muestra asociados, un árbol filogenético y/o asignación taxonómica de las OTUs. Este paquete aprovecha muchas de las herramientas disponibles en R para ecología y análisis filogenético (vegan, ade4, ape, picante), al mismo tiempo que utiliza sistemas gráficos avanzados y flexibles (ggplot2) para producir fácilmente gráficos de calidad de publicación de datos filogenéticos complejos ([McMurdie and Holmes 2013](#ref-mcmurdie2013phyloseq)). Mediante Phyloseq se puede llevar así a cabo la importación de un conjunto diverso de formatos de datos de secuenciación de microbiomas, su normalización, la visualización y el análisis estadístico ([McMurdie and Holmes 2013](#ref-mcmurdie2013phyloseq); [Callahan et al. 2016](#ref-callahan2016dada2)).

**Phyloseq** es especialmente útil para el análisis de datos de secuenciación de alto rendimiento, que a menudo son difíciles de manejar con los métodos tradicionales ([McMurdie and Holmes 2013](#ref-mcmurdie2013phyloseq); [Callahan et al. 2016](#ref-callahan2016dada2); [Thompson et al. 2017](#ref-thompson2017second)). Además, proporciona una serie de visualizaciones gráficas que son útiles para explorar y entender los datos de microbiomas ([McMurdie and Holmes 2013](#ref-mcmurdie2013phyloseq); [Callahan et al. 2016](#ref-callahan2016dada2); [Thompson et al. 2017](#ref-thompson2017second)).

A través de esta herramienta también facilita la investigación reproducible al permitir que los análisis se realicen en el entorno de programación de R. Esto permite que los análisis se documenten y compartan fácilmente, como en este mismo blog, lo cual facilita la colaboración y la revisión de los análisis ([McMurdie and Holmes 2013](#ref-mcmurdie2013phyloseq); [Callahan et al. 2016](#ref-callahan2016dada2)).

## Aplicaciones de Phyloseq

**Phyloseq** se utiliza en una amplia gama de aplicaciones, desde la ecología microbiana hasta la medicina. Por ejemplo, se ha empleado para analizar la diversidad microbiana en diferentes entornos, como el suelo ([Thompson et al. 2017](#ref-thompson2017second)), el agua ([Logares et al. 2014](#ref-logares2014metagenomic)) o el mismo cuerpo humano ([Consortium 2012](#ref-human_microbiome_project_consortium2012structure)). En medicina, Phyloseq se ha utilizado para analizar la relación entre el microbioma humano y diversas enfermedades, como la enfermedad inflamatoria intestinal ([Gevers et al. 2014](#ref-gevers2014treatment)) y la obesidad ([Le Chatelier et al. 2013](#ref-le_chatelier2013richness)).

# Instalación de Phyloseq

Es posible instalar Phyloseq fácilmente utilizando Bioconductor como se muestra a continuación ([Layeghifard, Hwang, and Guttman 2017](#ref-layeghifard2017disentangling); [“Bioconductor: Open Source Software for Bioinformatics” 2023](#ref-bioconductorweb)).

``` r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("phyloseq")
```

# Conclusión

Phyloseq es una herramienta poderosa y flexible para el análisis de datos de secuenciación de microbiomas. Proporciona una amplia gama de funciones para importar, analizar y visualizar estos datos, y es especialmente útil para el análisis de datos de secuenciación de alto rendimiento. Al permitir que los análisis se realicen en el entorno de programación de R, Phyloseq también facilita la investigación reproducible.

# Referencias

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-bioconductorweb" class="csl-entry">

“Bioconductor: Open Source Software for Bioinformatics.” 2023. Bioconductor. <https://bioconductor.org/packages/release/bioc/html/phyloseq.html>.

</div>

<div id="ref-callahan2016dada2" class="csl-entry">

Callahan, Benjamin J, Paul J McMurdie, Michael J Rosen, Andrew W Han, Amy Jo A Johnson, and Susan P Holmes. 2016. “DADA2: High-Resolution Sample Inference from Illumina Amplicon Data.” *Nature Methods* 13 (7): 581–83.

</div>

<div id="ref-human_microbiome_project_consortium2012structure" class="csl-entry">

Consortium, Human Microbiome Project. 2012. “Structure, Function and Diversity of the Healthy Human Microbiome.” *Nature* 486 (7402): 207–14.

</div>

<div id="ref-gevers2014treatment" class="csl-entry">

Gevers, Dirk, Subra Kugathasan, Dan Knights, Aleksandar D Kostic, Rob Knight, and Ramnik J Xavier. 2014. “Treatment-Naive Crohn’s Disease Patients Demonstrate Abnormalities in Microbial Community Structure and Function.” *Gut* 63 (12): 1928–37.

</div>

<div id="ref-layeghifard2017disentangling" class="csl-entry">

Layeghifard, Mehdi, David M Hwang, and David S Guttman. 2017. “Disentangling Interactions in the Microbiome: A Network Perspective.” *Trends in Microbiology* 25 (3): 217–28. <http://www.cell.com/article/S0966842X16301858/pdf>.

</div>

<div id="ref-le_chatelier2013richness" class="csl-entry">

Le Chatelier, Emmanuelle, Trine Nielsen, Junjie Qin, Edi Prifti, Falk Hildebrand, Gwen Falony, Mathieu Almeida, et al. 2013. “Richness of Human Gut Microbiome Correlates with Metabolic Markers.” *Nature* 500 (7464): 541–46.

</div>

<div id="ref-logares2014metagenomic" class="csl-entry">

Logares, Ramiro, Shinichi Sunagawa, Guillem Salazar, Francisco M Cornejo-Castillo, Isabel Ferrera, Hugo Sarmento, Pascal Hingamp, et al. 2014. “Metagenomic 16S rDNA Illumina Tags Are a Powerful Alternative to Amplicon Sequencing to Explore Diversity and Structure of Microbial Communities.” *Environmental Microbiology* 16 (9): 2659–71.

</div>

<div id="ref-mcmurdie2013phyloseq" class="csl-entry">

McMurdie, Paul J, and Susan Holmes. 2013. “Phyloseq: An r Package for Reproducible Interactive Analysis and Graphics of Microbiome Census Data.” *PloS One* 8 (4): e61217.

</div>

<div id="ref-thompson2017second" class="csl-entry">

Thompson, Luke R, Jon G Sanders, Daniel McDonald, Amnon Amir, Joshua Ladau, Kenneth J Locey, Robert J Prill, et al. 2017. “A Communal Catalogue Reveals Earth’s Multiscale Microbial Diversity.” *Nature* 551 (7681): 457–63.

</div>

</div>
