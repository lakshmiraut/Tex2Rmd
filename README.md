# Tex2Rmd

The article describes the typical features of a Latex document that this package can convert to the Rmarkdown format. The converted markdown document, possibly after further addition of other R chunks and edits, can be converted to html and word documents using R package knitr. It is also possible to convert it back to Latex, but you may have to tweak it a little to make the latex output look nice. 

**Keywords:** Latex, html, Rmarkdown, Microsoft word. 
# 1. Introduction 
This article uses bits and pieces of Latex contents from my own papers to illustrate features of this package. It is important to *emphasize* in **bold text that NOT ALL** features involving complex formatting codes in the Latex can be converted. It will convert only those that it is able to convert and the rest will be left alone. It incorporates basic minimum features generally used in a Ph.D. thesis, scientific article or a book. See this footnote^[It does not convert latex tables completely. This version of the software only creates a template for table with caption and label, you need to fill in the details in R markdown document.] for limitations on converting Latex table environment.

Section 2 describes how to get the software and use it. It runs under 32bit or 64bit windows 7, 8, 10 and 64bit Linux operating system. I programmed it in C++ and Java. In future, I will develop an R package that can combine knitr step to produce directly html file.  The steps are simplified to minimum of just downloading an exec file meant for your operating system and running it on your Latex file. The rest of the article describes various features of Latex document, it can convert. 
 
Section 3 discusses how it converts references. Section \@ref(sec4) shows what kind of equations both displayed and inline are converted. Pretty much it converts all math formats. 

Details can be found in [https://github.com/lakshmiraut/Tex2Rmd/releases/download/V0.1/Temp1.pdf](https://github.com/lakshmiraut/Tex2Rmd/releases/download/V0.1/Temp1.pdf)

# 2. Installation and Running 
The software runs on 32bit and 64bit windows and 64bit Linux operating systems.  Just download the exec file for your operating system and run it. You can find the exec files here [https://github.com/lakshmiraut/Tex2Rmd/releases/tag/V0.1](https://github.com/lakshmiraut/Tex2Rmd/releases/tag/V0.1). In this directory, you can also find a pdf file Temp1.pdf created using xelatex on the source file Temp1.tex, and also the R markdown, html and word files created by this program (creating Rmd file) and knitr in R or Rstudio (creating html and docx files).

Easiest way to start is to run the exec file by typing tex2rmd. It will show it's usage as below:

usage: tex2rmd inputTexFileName.tex -b bibFile.bib -o outputRmdFileName.Rmd 

where inputTexFileName.tex is the name of the source tex file. The rest are optional. If you did not provide the rest, it will not use any bibliography file (which you can add later) and also it will save the Rmd file in the source text directory with the same file name appending "-converted" and with file extension Rmd.  

-b bibFile.bib means user provides a bibliography file, which in this example is named bibFile.  It can use only bibliography files in bibTex format. This you specify if you have references in your document.

-o outputRmdFileName.Rmd means user provides a name the the R markdown file. If it is not provided, then the program will create a file in the same directory with the same source filename with -converted appended with extension Rmd in the same directory as the source file.

Next step:You can edit and add R markdown chunks and then use knitr to convert the Rmd file to html or word document.  

As an example, I used Example1.tex and bibFile1.bib, and ran  

tex2rmd Example1.tex -b bibFile1.bib  

creates Example1-converted.Rmd. You can download those files to a directory of your choice and ran the above command.  If you want to convert this Rmd file to other formats, you also need to download any other files it refers to, in this case tree1.png file. I then use knitr on the file Example1-converted.Rmd to create html file Example1-converted.html. You can also create word document using the appropriate yml commands on the top of the Rmd file. 

