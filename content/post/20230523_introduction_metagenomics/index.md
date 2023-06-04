---
title: "Introducción a la Metagenómica"
date: "2023-05-23T21:48:51-07:00"
tags: ["Bioconductor", "Phyloseq", "Metagenomics"]
output: html_document
bibliography: metagenomics.bib
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

# Introducción

La metagenómica es un subcampo de la genómica que ha surgido como una disciplina emergente que se centra en el análisis del material genético de las comunidades microbianas presentes en los ecosistemas naturales de forma directa, esto es, en lugar de centrarse en un solo organismo, esta rama científica pone el foco en el estudio de la diversidad y la función de las comunidades microbianas en su conjunto ([Handelsman 2004](#ref-Handelsman2004)). Este enfoque permite el estudio de los microorganismos en su hábitat natural, sin la necesidad de cultivarlos en el laboratorio. Es así cómo la metagenómica ha revolucionado nuestra comprensión de la diversidad y la funcionalidad de las comunidades microbianas ([Wooley, Godzik, and Friedberg 2010](#ref-Wooley2010)).

## Metagenómica: Secuenciación de Nueva Generación (NGS)

La metagenómica, como se ha mencionado, es el estudio de los genomas de comunidades microbianas directamente a partir de muestras ambientales, sin la necesidad de cultivar organismos individuales en el laboratorio ([Handelsman 2004](#ref-Handelsman2004)). Esta disciplina ha experimentado un crecimiento significativo en las últimas dos décadas, impulsado en gran medida por los avances en las tecnologías de secuenciación de nueva generación (NGS) ([Margulies et al. 2005](#ref-Margulies2005)).

Las tecnologías de Secuenciación de Nueva Generación (NGS) han revolucionado la genómica y la metagenómica, permitiendo la secuenciación de millones de fragmentos de ADN simultáneamente ([Mardis 2008](#ref-Mardis2008)). Esto ha permitido un aumento sin precedentes en la velocidad y la economía de la secuenciación del genoma, lo que a su vez ha permitido el análisis metagenómico a gran escala de comunidades microbianas ([Metzker 2010](#ref-Metzker2010)).

# Metagenómica: Estado del Arte

La metagenómica presenta varios desafíos computacionales, incluyendo la necesidad de manejar grandes volúmenes de datos y la dificultad de asignar secuencias a especies específicas([Wooley, Godzik, and Friedberg 2010](#ref-Wooley2010)). A pesar de estos desafíos, la metagenómica ha proporcionado una visión sin precedentes de la diversidad y la funcionalidad de las comunidades microbianas ([Wooley, Godzik, and Friedberg 2010](#ref-Wooley2010)).

## Unidades Taxonómicas Operativas (OTUs)

Este avance ha venido de la mano de un nuevo sistema de clasificación, las **Unidades Taxonómicas Operativas** (**OTUs**). Las OTUs son una forma de clasificar los grupos de secuencias de ADN similares que se supone que representan una especie o un grupo de especies estrechamente relacionadas, lo cual permite navegar en estos grandes volúmenes de datos muestreados ([Schloss et al. 2009](#ref-Schloss2009)). Las OTUs son fundamentales para la comparación de la diversidad y composición de las comunidades microbianas en diferentes muestras ([Huse et al. 2008](#ref-Huse2010)).

## Crecimiento de la Metagenómica

La metagenómica ha experimentado un rápido desarrollo y evolución en los últimos años. Los avances en las tecnologías de secuenciación y análisis de datos han permitido un análisis más profundo y preciso de las comunidades microbianas ([Knight et al. 2018](#ref-Knight2018)).

Este crecimiento explosivo de la metagenómica ha sido facilitado en gran medida por herramientas como **USEARCH**. Esta herramienta de análisis de secuencias genéticas proporciona algoritmos de búsqueda y agrupación de alta velocidad, superando a **BLAST** en términos de eficiencia. Al combinar múltiples algoritmos en un solo paquete, **USEARCH** optimiza la productividad y facilita la exploración de datos genéticos, lo que es esencial en el campo de la metagenómica ([USEARCH 2023](#ref-usearch2023); [Altschul 1997](#ref-Altschul1997)).

Un estudio reciente de Rognes et al. (2020) ha demostrado que **VSEARCH**, una herramienta de análisis metagenómico, es generalmente más preciso que USEARCH cuando se realiza la búsqueda, el agrupamiento, la detección de quimeras y el muestreo ([Rognes et al. 2020](#ref-Rognes2020)). Además, VSEARCH es más rápido que USEARCH cuando se realiza la dereplicación y la fusión de lecturas de extremo a extremo, aunque es más lento para el agrupamiento y la detección de quimeras ([Rognes et al. 2020](#ref-Rognes2020)).

## Herramientas bioinformáticas en metagenómica

Como ya se ha explicado, las herramientas bioinformáticas son esenciales para el análisis de los datos metagenómicos. Estas herramientas permiten el ensamblaje de las secuencias de ADN, la predicción de genes, la anotación funcional y la comparación de comunidades microbianas. Algunas de las herramientas más utilizadas en metagenómica incluyen MetaVelvet, IDBA-UD, Ray Meta y CONCOCT ([Rice et al. 2017](#ref-Rice2017)).

Una herramienta bioinformática muy importante que se utilizan en la metagenómica, es **QIIME**, que permite el análisis de datos de secuenciación de comunidades de alta densidad ([Caporaso et al. 2010](#ref-Caporaso2010)). Otras herramientas importantes incluyen MetaVelvet, que se utiliza para el ensamblaje de metagenomas, y Phyloseq, que proporciona una serie de herramientas para el análisis de datos de secuenciación de comunidades microbianas ([Quince et al. 2017](#ref-Quince2017)).

# Conclusión

La metagenómica ha revolucionado nuestra capacidad para estudiar las comunidades microbianas, permitiéndonos explorar la diversidad microbiana a una escala y profundidad sin precedentes revolucionando así nuestra comprensión de los microorganismos y su papel en nuestro mundo. Los avances en las tecnologías de secuenciación y análisis de datos están impulsando continuamente los límites de lo que es posible en la metagenómica, permitiendo una comprensión cada vez más profunda y matizada de los complejos ecosistemas microbianos que nos rodean y habitan dentro de nosotros.

# Referencias

<div id="refs" class="references csl-bib-body hanging-indent">

<div id="ref-Altschul1997" class="csl-entry">

Altschul, S. 1997. “Gapped BLAST and PSI-BLAST: A New Generation of Protein Database Search Programs.” *Nucleic Acids Research* 25: 3389. https://doi.org/<https://doi.org/10.1093/nar/25.17.3389>.

</div>

<div id="ref-Caporaso2010" class="csl-entry">

Caporaso, J. G., J. Kuczynski, J. Stombaugh, K. Bittinger, F. D. Bushman, E. K. Costello, A. G. Fierer N. andPeña, J. K. Goodrich, J. I. Gordon, et al. 2010. “QIIME Allows Analysis of High-Throughput Community Sequencing Data.” *Nature Methods* 7 (5): 335–36.

</div>

<div id="ref-Handelsman2004" class="csl-entry">

Handelsman, J. 2004. “Metagenomics: Application of Genomics to Uncultured Microorganisms.” *Microbiology and Molecular Biology Reviews* 68 (4): 669–85.

</div>

<div id="ref-Huse2010" class="csl-entry">

Huse, S. M., L. Dethlefsen, J. A. Huber, D. Mark Welch, D. A. Relman, and M. L. Sogin. 2008. “Exploring Microbial Diversity and Taxonomy Using SSU rRNA Hypervariable Tag Sequencing.” *PLoS Genetics* 4 (11): e1000255.

</div>

<div id="ref-Knight2018" class="csl-entry">

Knight, R., A. Vrbanac, B. C. Taylor, A. Aksenov, C. Callewaert, J. Debelius, A. Gonzalez, et al. 2018. “Best Practices for Analysing Microbiomes.” *Nature Reviews Microbiology* 16 (7): 410–22.

</div>

<div id="ref-Mardis2008" class="csl-entry">

Mardis, E. R. 2008. “Next-Generation DNA Sequencing Methods.” *Annual Review of Genomics and Human Genetics* 9: 387–402.

</div>

<div id="ref-Margulies2005" class="csl-entry">

Margulies, M., M. Egholm, W. E. Altman, S. Attiya, J. S. Bader, L. A. Bemben, J. Berka, et al. 2005. “Genome Sequencing in Microfabricated High-Density Picolitre Reactors.” *Nature* 437 (7057): 376–80.

</div>

<div id="ref-Metzker2010" class="csl-entry">

Metzker, M. L. 2010. “Sequencing Technologies - the Next Generation.” *Nature Reviews Genetics* 11 (1): 31–46.

</div>

<div id="ref-Quince2017" class="csl-entry">

Quince, C., A. W. Walker, J. T. Simpson, N. J. Loman, and N. Segata. 2017. “Shotgun Metagenomics, from Sampling to Analysis.” *Nature Biotechnology* 35 (9): 833–44.

</div>

<div id="ref-Rice2017" class="csl-entry">

Rice, G., R. D. Stedtfeld, T. Stedtfeld, J. M. Tiedje, and S. A. Hashsham. 2017. “The Future of Metagenomics in Microbial Ecology.” *Microbial Ecology* 74 (2): 227–40.

</div>

<div id="ref-Rognes2020" class="csl-entry">

Rognes, T., T. Flouri, B. Nichols, C. Quince, and F. Mahé. 2020. “VSEARCH: A Versatile Open Source Tool for Metagenomics.” *PeerJ* 4: e2584.

</div>

<div id="ref-Schloss2009" class="csl-entry">

Schloss, P. D., S. L. Westcott, T. Ryabin, J. R. Hall, M. Hartmann, E. B. Hollister, R. A. Lesniewski, et al. 2009. “Introducing Mothur: Open-Source, Platform-Independent, Community-Supported Software for Describing and Comparing Microbial Communities.” *Applied and Environmental Microbiology* 75 (23): 7537–41.

</div>

<div id="ref-usearch2023" class="csl-entry">

USEARCH. 2023. “USEARCH.” <https://www.drive5.com/usearch/download.html>.

</div>

<div id="ref-Wooley2010" class="csl-entry">

Wooley, J. C., A. Godzik, and I. Friedberg. 2010. “Metagenomics: Facts and Artifacts, and Computational Challenges.” *Journal of Computer Science and Technology* 25 (1): 71–81.

</div>

</div>
