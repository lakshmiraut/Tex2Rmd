# Tex2Rmd

A package to covert LaTex document to Rmarkdown format for further processing and then to convert into html, Microsoft Word or back to LaTex format. 

The article describes a typical features of a Latex document that can be converted to the Rmarkdown format using this package. The converted markdown document, possibly after further addition of other R chunks, can be converted to html and word documents. It is also possible to convert back to Latex, but you may have to tweak it a little to make the latex output look nice. 

# Introduction {#sec1}
This article uses bits and pieces Latex contents from my own papers to illustrate features of this package. The binaries are given for windows (32bit should also work for 64bit and Linux 64bit). It is important to *emphasize* in bold text **NOT ALL** features involving complex formatting codes can be converted.  It incorporates the basic minimum features that are generally used in a Ph.D. thesis, scientific article or a book. See this footnote^[It does not convert latex tables completely. This verion of the software only creates a template for table with caption and label, you need to fill in the details in Rmarkdown document.] for limitations on converting Latex table environment.

Section \@ref(sec2) discusses how it converts references. Section \@ref(sec3) shows what kind of equations both displayed and inline are converted. Section \@ref(sec4) shows conversions of figures and tables. Section \@ref(sec5) describes the list like environments such as itemize, enumerate and description. These environments may be present inside other environments such as in proposition, theorem etc, as shown in Section \@ref(sec6). Conversions of list environments are not perfect, you may need some tweaking in the converted Rmarkdown document. Section \@ref(sec6) shows theorem like Latex environments such as Theorem, Lemma, Proposition each with its own auto numbering and proof like environments without numbering. Section \@ref(sec7) discusses a few important facts and how to do remarks.



# Referencing {#sec2}
The main findings in [@Aalen.etal_2008_Book;@Kanherkar.etal_2014] are that .... For the effects of early childhood factors on school and labor market outcomes, see @Heckman.Raut_2016, and also see @Raut_2018 with an updated references. In machine learning, [@Altae-Tran_2016;@Altae-Tran.etal_2017] show how an RNN can be used with limited data. 
