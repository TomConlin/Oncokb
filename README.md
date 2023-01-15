

# Oncokb AA replacment choices 

## Reverse Translation 
Translating from mRNA to amino acids is straight forward and deterministic.
A sequence of three nucleic acid bases is taken as a codon which is
translated into a amino acid according to the
[standard genetic code](https://en.wikipedia.org/wiki/Genetic_code#Standard_codon_tables).

However, given the replacement of a single amino acid for another,
in the worst case, there could be as many as 36 different sets
of nucleic acid changes applied to the codon,
each of which could be responsible.

Here [Oncokb](http://oncokb.org) API for variants (lic. has been tightened down)
 is giving us amino acid replacements within a gene
and information on the consequences and we would like to find a way
to link back to variant sources which necessitates determining
the underlying nucleic changes to the codon producing the amino replacement.

Since Oncokb gives a curated isoform and an offset we should be able to figure
out if the codon at the ofset in the mRNA matches the reported reference Amino
(so far, not realiably) which eliminates any of the codon replacement choices
which do not begin with the observed codon.



---
## Julia
In recognition of my favorite upcoming programming language
[Julia](https://julialang.org/)
receiving over 5 million in grants for continued development his week
I did this jupyter notebook with iJulia.
(just as I did my first ever notebook in Julia several years ago)  

Note. this is not a call or recommendation for language hopping.  
Julia is still in beta which means breaking changes on new releases.
So even if we decide it has really neat features we would like to use
we should not begin adopting till after version 1.0, 
which if road maps are to be believed won't happen before the end of this year.
