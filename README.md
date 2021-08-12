# Tesefameb
 Repositório com modelo RMarkdown para trabalhos acadêmicos da FAMEB/UFBA
 Este projeto é insipirado no [thesisdown](https://github.com/ismayc/thesisdown), [coppedown](https://github.com/COPPE-UFRJ/coppedown), [ourcodingclub](https://ourcodingclub.github.io) 

## Usando o modelo para escrever seu trabalho.

[R](https://cran.r-project.org/)
[RStudio](https://rstudio.com/)

É necessário o LaTeX para gerar os arquivos em pdf. A forma mais fácil é instalar diretamente no R usando o pacote [`tinytex`]((https://yihui.name/tinytex/))

```
install.packages(c('tinytex', 'rmarkdown'))
tinytex::install_tinytex()
# after restarting RStudio, confirm that you have LaTeX with 
tinytex:::is_tinytex()
# install additional needed latex packages
tinytex::tlmgr_install("babel-portuges")

```
Recomendo trocar o repositório CTAN do tinytex para algum localizado no Brasil. Isso pode ser feito da seguinte forma:

```
tinytex::tlmgr(c('option', 'repository',
'http://linorg.usp.br/CTAN/systems/texlive/tlnet/'))
```
Para melhor formatação dos códigos:
instalar a biblioteca formatR
```{r, echo = F}
library(knitr)
opts_chunk$set(tidy.opts=list(width.cutoff=80),tidy=TRUE)
```


Os parâmetros da capa/contra-capa estão no arquivo Tese e na sua maioria em LaTeX.
As outras seções podem ser editadas em markdown normalmente.
