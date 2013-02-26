opts_chunk$set(warning=FALSE, message=FALSE, comment=NA, cache=FALSE)

---
name: networks-phylogeny
layout: post
title: Networks phylogeny
date: 2013-01-24
author: Scott Chamberlain
tags: 
- R
- data
- phylogenetics
---

Made a phylogeny ecologist style. 
***************
That is, I: 

1. Created a topology using [Mesquite software] from published phylogenies, then
2. Got node age estimates from [timetree.org](http://timetree.org/) (p.s. Wish I could use the new [http://datelife.org/](http://datelife.org/), but there isn't much there quite yet), then
3. Used bladj function in phylocom to stretch out the branch lengths based on the node estimates.

Unfortunately, this process can't all be collected in an R script, but below is the process I followed, which hopefully makes it more reproducible.

***************

### Notes on which published phylogenies were used for constructing the topology
+ Arthropods based on 
	+ Ishiwata et al. 2010 MolPhyloEvol
+ Hymenoptera topology based on
	+ Heraty et al. 2011 Mol. Phy. Evol, Fig. 1 Bayesian phylogeny
+ Vespidae based on
	+ Mines et al. 2007 PNAS
+ Bees based on 
	+ Overall: Danforth et al. 2006 PNAS
	+ Megachilidae: Gonzalez et al. 2012 SystEntomol
	+ Apidae: Cardinal et al. 2010 PNAS
	+ Andrenidae: Danforth et al. 2013 AnnRevEntomol - Fig. 5
	+ Halictidae: Danforth et al. 2013 AnnRevEntomol - Fig. 6
	+ Colletidae: not needed, only 2 species
+ Coleoptera based on 
	+ Hunt et al. 2007 Science
+ Lepidoptera based on
	+ Overall: 
		+ Mutanen et al. 2010 PRSLB
		+ Kim et al. 2011 Mol. Phyl. Evol. 
	+ Nymphalidae: Freitas & Brown 2004 Syst. Biol. - Figure 3
+ Hemiptera based on
	+ Cryan and Urban 2011 Systematic Entomology - Figure 2
+ Diptera based on
	+ Overall: Wiegmann et al. 2011 PNAS - Figure 1
	+ Bombyliidae: Yeates 1994 Bull. Amer. Mus. Nat. Hist.
	+ Syrphinae: Mengual et al. 2007 Cladistics

### TimeTree used to get node ages for phylogeny
+ [website](http://timetree.org/), [here's a link]() to the node ages I used.

### Used bladj command in phylocom to stretch out branches to get branch lengths, as:
`./phylocom bladj > out.txt`

***************

The phylogeny (visualized in FigTree, many nodes are collapsed, it has about 500 species):

![center](https://raw.github.com/SChamberlain/schamberlain.github.com/master/img/phylogeny.png)

*********
#### Get the .Rmd file used to create this post [at my github account](https://github.com/SChamberlain/scott/blob/gh-pages/_drafts/2013-01-24-networks-phylogeny.Rmd) - or [.md file](https://github.com/SChamberlain/scott/blob/gh-pages/_posts/2013-01-24-networks-phylogeny.md).

#### Written in [Markdown](http://daringfireball.net/projects/markdown/), with help from [knitr](http://yihui.name/knitr/).
