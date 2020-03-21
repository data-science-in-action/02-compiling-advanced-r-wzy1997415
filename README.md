#### Introduction 
###### README.Rmd--problems(errors) and solutions
###### index.html--the result of compilation
Problems and solutions

During the building process, the followings are the errors I've met and how I solved them.

#### **1、Use devtools install sloop and emo**

**（1）**`install.packages("sessioninfo")`.

**（2）**Install R Package dependencies using `devtools::install_github("hadley/sloop")` and `devtools::install_github("hadley/emo")`. 
**（3）**Use`bookdown::render_book("index.Rmd", output_format = "bookdown::pdf_book")` to compile the book.



#### **2、Lacking packages**

**(1)Introduction.Rmd**

**Error**  in loadNamespace(name) : there is no package called 'desc'

--`install.packages("desc")`

**Error**  in loadNamespace(name) : there is no package called 'sessioninfo'

--`install.packages("sessioninfo")`

**Error**  in library(lobstr) : there is no package called 'lobstr'--`install.packages("lobstr")`

**(2)Conditions.Rmd**

**Error**  in library(testthat) : there is no package called 'testthat'

--`install.packages("testthat")`

**(3)Functionals.Rmd **
**Error** in loadNamespace(name) : there is no package called 'tibble'

--`install.packages("tibble")`

**(4)R6.Rmd**

**Error** in loadNamespace(name) : there is no package called 'DBI'

--`install.packages("DBI")`

**Error** in loadNamespace(name) : there is no package called 'RSQLite'

--`install.packages("RSQLite")`

**(5)Perf-measure.Rmd**

**Error** in library(profvis) : there is no package called 'profvis'
--`install.packages("profvis")`

**Error** in loadNamespace(name) : there is no package called 'ggbeeswarm'

--`install.packages("ggbeeswarm")`

In summary, I installed the following packages, named desc,sessioninfo,lobstr,testthat,emo,tibble,sloop,DBI,RSQLite,dbplyr,profvis,bench and ggbeeswarm. 



#### **3、Introduction.Rmd**

**Error** in cat(paste0(contributors$desc, collapse = ", "))

**Adding** `encoding="UTF-8"`to line 224.
The full command is: `contributors <- read.csv("contributors.csv", stringsAsFactors = FALSE,encoding = "UTF-8")` 



#### **4、Rcpp.Rmd**
In this session, a working C++ compiler is needed. To get it: On Windows, install Rtools.The installation tutorial can refer to this website<https://blog.csdn.net/wzgl__wh/article/details/70185687>



#### **5、"xelatex" not Found**

Use *tinytex* to install *TinyTex* might can't solve the problem, so I used *MiKTeX* instead.



#### **6、Package fontspec Error: The font "Inconsolata" and "Andale Mono" cannot be found.**

Download the *Inconsolata* font and *Andale Mono* font, and place them in the C:/Windows/Fonts folder.
