# PcircRNA_finder
PcircRNA_finder: a software for circRNA prediction in plants

  Recent studies in animals have found a kind of non-coding RNA molecule called circular RNA (circRNA) produced by splicing complex with one or more exons of the gene. In animals and human cells, circular RNA has miRNA sponge function, regulating its parent gene functions and also it was reported that the formation of circular RNA depends on both sides of the intron complementary sequence. However, the situation of circular RNA in plants is unknown. Using the current softwares or algorithms developed for animals or humans, the accuracy of the prediction of circular RNA in plant is relatively low and the sensitivity is not high. Here, a new circRNA prediction method called PcircRNA_finder is developed in plants. Using the simulated data and real RNA-seq data, we show that the software has good sensitivity, and can be more comprehensive to find out the circular RNA. It can be used to distinguish and predict circular RNA with alternative donor/acceptor sites with minor changes. At the same time, the software has a better output, and gives a more detailed information on the circular RNA, which facilitate the follow-up of experimental verification and the functional study of circular RNA.

	PcircRNA_finder is mainly designed for exonic circRNA prediction (Figure 1), which consists of three parts: 
	(1) Catchor: Catchor is used to collect as many backsplice sites as possible, which are supported by chiastic clipping mapping based on many available fusion detection methods, including Tophat-Fusion (Kim and Salzberg, 2011), STAR-Fusion (Dobin, et al., 2013), find_circ (Memczak et al., 2013), Mapsplice (Wang, et al., 2010), segemehl (Hoffmann, et al., 2014). Among these candidate back-splice sites, it has many false positive sites for specific sofware and then, depends on next Filter module to filter it out.
 	(2) Annotator: Annotator can be used to annotate the candidate sites with gene structure annotation, which compares the back-splice sites to the exon-intron boundary. And It's based on two experimental observations, one is that the experimental verified circRNAs (10/18) in rice are consistent with exon boundary (Ye, et al., 2015), which shows circRNA used same splicing site with pre-mRNA splicing; the other is that the biogensis of circRNA is dependent on canonical spliceosomal machinery even though circRNA's back-splicing site is cryptic and flexible (Starke, et al., 2015). That's to say, circRNA is another form of alternative splicing. 
	(3) Filter: Filter is used to prioritize the above candidate circRNA. It has two parts: filtering the candidate circRNAs with two kinds of splicing signal, namely U2 based spliceosome (usually with consensus sequence GT-AG and GC-AG ) and U12 based minor spliceosome (usually with consensus sequence AT-AC) (Reddy, et al., 2013; Staiger and Brown, 2013); creating a pseudoRef with chiastic backsplice site flanking sequences and then mapping raw reads to it to check the back-splice sites.


# Reference
Chen et al., PcircRNA-finder: a program to identify circular RNAs in plants. Bioinformatics. 2016
https://academic.oup.com/bioinformatics/article-lookup/doi/10.1093/bioinformatics/btw496
