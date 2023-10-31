# Overview of maser
- Alternative splicing creates novel splice isoforms - functional interpretion of splicing requires the transcriptomic and proteomic information
- maser: package to enable functional characterization of splicing in both transcriptomic and proteomic
- maser: use rMATS result to:
+ Filter rMATS splicing events based on RNA-seq coverage, p value and differential percent spliced-in (PSI)
+ Analysis of global splicing effects using boxplots, PCA and volcano plots
+ Mapping splicing events to Ensembl transcripts and UniprotKB proteins
+ Integration with UniprotKB for annotation of protein features overlapping splicing events
+ Visualization of transcripts and protein affacted by splicing using Gviz plots
- Mapping the splicing events to protein features such as topological domains, motifs and mutation sites provided by UniprotKB and visualized along the genomic location of splicing

 ## Importing rMATS events
 Step 1: import splicing events by using maser() function: indicating the path of rMATS files and labels for conditions. This function will returns an object containing all events quantified by rMATS
> library(maser)
> library(rtracklayer)
> path <- system.file("extdata", file.path("MATS_output"), package = "maser") 
> hypoxia <- maser(path, c("Hypoxia 0h", "Hypoxia 24h"), ftype = 
> 
