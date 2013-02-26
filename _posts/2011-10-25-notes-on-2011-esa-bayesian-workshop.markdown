---
layout: post
title: Notes on 2011 ESA Bayesian workshop
post_id: 615
tags: 
- Uncategorized
---

<div>Bayesian Workshop ESA 2011
<ul>
	<li>Influence of the prior: when small data set prior can influence analysis greatly, whereas when large data set prior influences analysis less</li>
</ul>
<ul>
	<li>The mode of a posterior estimate is (or is sometimes?) equal to the Max. Likelihood estimate</li>
</ul>
<ul>
	<li>A special case of the beta distribution (1,1?) gives a uniform distribution - so perhaps don't need to specify a uniform distribution specifically</li>
</ul>
Hierarchical Bayesian Models
<ul>
	<li>No analytical solution for posterior or marginal dist, so MCMC numerical simulation (or max lik.)</li>
</ul>
<ul>
	<li>MCMC: Gibbs or Metropolis-Hastings</li>
</ul>
BUGS
<ul>
	<li>Similar: # sign for comments;</li>
</ul>
<ul>
	<li>Dissimilar: BUGS uses 'precision' instead of variance/sd in e.g., lognorm(mu, sd); BUGS never uses equals signs (unless assigning data object); Don't put calculation within a function;</li>
</ul>
<ul>
	<li>Random variables (use '~'). Fixed variables (use '<-')</li>
</ul>
<ul>
	<li>load inits OR gen inits (can use either or both)</li>
</ul>
<ul>
	<li>If autocorrelation in MCMC chains, use Sample Monitor Tool -> Thin -> value of e.g., 20 to redudce autocorrelation</li>
</ul>
<ul>
	<li>Do the same code writing rules apply when in R packages for BUGS?:</li>
</ul>
<ul>
	<li>Capital "I(0,)" truncates the previous number to zero</li>
</ul>
<ul>
	<li>Data import: save from excel as 'ms-dos'? and 'END' at end of file</li>
</ul>
</div>