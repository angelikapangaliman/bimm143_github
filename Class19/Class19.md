# Class 19: Mini Project: Cancer Mutation Analysis


``` r
library(bio3d)

a <- read.fasta("A17475228_mutant_seq.fa")
```

``` r
aln <- rbind(a$wt_healthy, a$mutant_tumor)
dim(aln)
```

    NULL

``` r
wt <- toupper(a$wt_healthy)
mut <- toupper(a$mutant_tumor)

aln <- rbind(wt, mut)
```

``` r
library(bio3d)

s <- conserv(aln)

mutation.position <- which(s != 1)

mutation.position
```

    integer(0)

``` r
paste0(wt[mutation.position], mutation.position, mut[mutation.position])
```

    character(0)
