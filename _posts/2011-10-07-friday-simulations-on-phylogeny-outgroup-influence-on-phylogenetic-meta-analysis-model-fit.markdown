---
layout: post
title: Friday; simulations on phylogeny outgroup influence on phylogenetic meta-analysis model fit
post_id: 584
tags: 
- Evolution
- R
---

*Note to self: not sure if I did the simulation right....*

<span style="font-family:'Helvetica Neue', Helvetica, Arial, sans-serif;">Modeling: wanted to find out how an outgroup on a long branch (e.g., two species of plants are in a phylogeny where the remaining species are all animals) would influence model fit in phylogenetic meta-analysis. So I did like so:</span>

*Simulation details:*

**<span style="color:#000000;font-family:tahoma, sans-serif;">Simulated 100 trees under each of the two following conditions:</span>
<div><span style="color:#000000;"><span style="font-size:x-small;"><span style="font-family:tahoma, sans-serif;">-regular trees, randomly generated coalescent tree (in fig legend as "reg")</span></span></span></div>
<div><span style="color:#000000;"><span style="font-size:x-small;"><span style="font-family:tahoma, sans-serif;">-</span></span>outgroup added trees, randomly generated coalescent tree with two fewer species than a reg tree, then an outgroup of two species added on a long branch (in fig legend as "out")</span></div>
<div><span style="color:#000000;">Each of the above two cases were generated at 10, 20, 40, 60, 80, and 100 species. </span></div>
<div><span style="font-family:tahoma, sans-serif;color:#000000;">
</span></div>
<div><span style="font-family:tahoma, sans-serif;color:#000000;">I also evolved a trait on each tree (here, we assume this trait is the effect size), and created a dataset for each tree (with the effect size, variance set to 1 for each species, and no grouping variable).  This is perhaps not ideal...</span></div>
<div><span style="color:#000000;">
</span></div>
<div><span style="font-family:tahoma, sans-serif;color:#000000;">I then ran all these trees and datasets through Phylometa (from R of course), and plotted the AIC max lik model fit (left two panels) and the ratio of phy:trad max lik model fit (right two panels), for both fixed (top two panels) and random (bottom two panels) effects models. </span></div>
<div><span style="font-family:tahoma, sans-serif;color:#000000;">
</span></div>
<div><span style="font-family:tahoma, sans-serif;color:#000000;">The line fits are Loess, so no particular model was fitted there, just to help see the patterns. </span></div>
Here is the output from the simulation:

<img class="alignleft size-full wp-image-587" title="myplot" src="http://schamber.files.wordpress.com/2011/10/myplot.jpeg" alt="" width="584" height="584" />

_*Bottom line: It seems that indeed, an outroup on a long branch does make model fit worse. *_