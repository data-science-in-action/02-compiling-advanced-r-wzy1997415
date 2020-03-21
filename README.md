# Introduction and problems

Lacking packages
I installed the following packages, named desc,sessioninfo,lobstr,testthat,emo,tibble,sloop,DBI,RSQLite,dbplyr,profvis,bench and ggbeeswarm. Most of them can be installed by install.packages(), but emo can not. Check the following section Functionals.Rmd for more details.

Introduction.Rmd
For this session, there may be the following errors like lacking packages and invalid multibyte string.
Adding encoding = "UTF-8" in line 224 can fix it.


Functionals.Rmd
Lacking packages
Quitting from lines 96-103 (Functionals.Rmd) 
Error in loadNamespace(name) : there is no package called 'emo'

Quitting from lines 726-734 (Functionals.Rmd) 
Error in loadNamespace(name) : there is no package called 'tibble'
Install the package tibble by

install.packages("tibble")
OO.Rmd
Quitting from lines 5-7 (OO.Rmd) 
Error in library(sloop) : there is no package called 'sloop'
install.packages("sloop")
R6.Rmd
Quitting from lines 535-550 (R6.Rmd) 
Error in loadNamespace(name) : there is no package called 'DBI'
install.packages("DBI")
Quitting from lines 535-550 (R6.Rmd) 
Error in loadNamespace(name) : there is no package called 'RSQLite'
install.packages("RSQLite")
Big-picture.Rmd
Quitting from lines 209-221 (Big-picture.Rmd) 
Error: The dbplyr package is required to communicate with database backends.
Execution halted
Error in Rscript_render(f, render_args, render_meta) : 
  Failed to compile Big-picture.Rmd
Calls: <Anonymous> ... render_book -> render_new_session -> Rscript_render
Execution halted


Rcpp.Rmd
In this session, a working C++ compiler is needed. Then I install Rtools.
