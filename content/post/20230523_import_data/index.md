---
title: "Análisis de Metagenómica en R"
date: "2023-05-23T21:48:51-07:00"
tags: ["Bioconductor", "Phyloseq", "Metagenomics"]
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
    background-color: #F5F5F5;
    
}
pre {

    font-family: Serif;
    
}
</style>

# ¿Qué es Phyloseq?

Phyloseq es un paquete de R diseñado para facilitar la importación, el almacenamiento, el análisis y la visualización de datos de secuenciación filogenética complejos que ya han sido agrupados en Unidades Taxonómicas Operativas (OTUs)\[^3^\]. Phyloseq proporciona importación de datos de abundancia y datos relacionados de tuberías populares de eliminación de ruido / agrupamiento de OTU (DADA2, UPARSE, QIIME, mothur, BIOM, PyroTagger, RDP, etc.), envoltorios de análisis de conveniencia para tareas de análisis comunes, y 44 métodos de distancia soportados (UniFrac, Jensen-Shannon, etc.)\[^3^\].

# Instalación de Phyloseq

Phyloseq es un paquete de R que se puede instalar fácilmente utilizando Bioconductor\[^4^\]. Abajo se muestra el código que puedes usar para instalar Phyloseq:

``` r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("phyloseq")
```
