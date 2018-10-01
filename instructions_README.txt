Formatting is a pain in Microsoft Word, particularly with long, complex documents like a dissertation. LaTeX is a professional program used for typesetting and formatting books and journals articles (including most peer-review journals). The idea is you put in the text, tables, and figure, and latex uses a style file to format EVERYTHING. This will format an entire dissertation for the FIU Biology Department with ALL the specifications of UGS. This will automatically create title pages, table of contents, bibliographies, margins, everything to meet the UGS formatting standards. This file also creates a document where the reader can click references and figures to take them to the referenced citation. The cherry on top: most peer-review journals accept LaTeX files for manuscript submission, so you can turn around and use the same files for manuscript submission/review process. BTW, I altered files from the FIU Computer Science department, who altered files from Cornell's dissertation templates. Also, This dissertation has not been approved yet, so I won't trust any of the science or content. 

There is an obstacle for some: this is prompt line, code based program that looks and feels like scripting in R. Some people don't like that. With these directions and the attached templates, learning should be easy. Latex is made for Mac and PC. I use a Mac, take that into account.


First, Download MacTeX and install - https://www.latex-project.org/get/

Overview of LaTeX files: 

.tex files - these are the content files to typeset. This dissertation has 12 .tex files. The one titled "Thesis" is the one you should run. It will compile and stitch together all the other tex files. Each Chapter and other main sections (abstract, vita, etc) have their own file. Open these in a text editor (like sublime text 2, which is free for download).

.bib files - these are bibliography files for each chapter. Citation managers can export libraries in .bib format so you can easily makes these. Google scholar also has bibtex as one of the citation options. Each .bib file id referenced in the appropriate .tex file.

.cls file - this is the formatting/style file. It's set up for FIU dissertations.


Running Latex

There are two very different ways.

1) open terminal and change the directory to the one that contains all the Latex files. The command "pdflatex" will cause latex to run. In this case, run "pdflatex thesis" for the thesis file. Then run bibliography files for each tex file that cites references. Do this by running "bibtex"

bibtex intro
bibtex chap1
bibtex chap2
bibtex chap3
bibtex chap4
bibtex conclusions

run "pdflatex thesis" 3-4 more times. Each time you run this, parts of the table of contents get built.

A pdf file will be created in the directory. ya est‡. The nice thing about this method is that you can quickly rerun files if you notice a mistake or want to see how small adjustments look.

2) open the app "texshop" that was installed with MacTeX. Open the "thesis.tex" file in the drop down. Press "typeset". This will create a document but you'll notice the citations are all question marks. To fix this, open each of the tex files that cite references. Click the "Typeset" option from the menu in the top bar. It'll dropdown and then click "bibtex". It won't look like anything happened but an .aux file will be formed to fix citations. Now go back to the "thesis.tex" file and click typeset. If the table of contents looks strange, click typeset a few more times.

The nice thing about this method is if there is a coding problem, you can click the "go to error" button, to immediately find it.


User Tips.

use find-and-replace to change everything at once. This beats going through the document and changing CO2 to CO\textsubscript{2} every time 

This format uses "natbib" for references. This allows for different types of in-text citations for example:

\citet{jon90} -> Jones et al. (1990)
\citep{jon90} -> (Jones et al., 1990)
\citealt{jon90} -> Jones et al. 1990


There will probably be minor problems with the bibliography. Fix these in the .bib files. But you have to re-run the bibtex file then re-run the tex file before you see changes. For example, a problem in the chapter 2 bibliography is corrected by fixing the problem in the bib file, then running "bibtex chap2" then "pdflatex thesis".

All the figures are divided by chapters in the figures folder. Use the pdf format for figures and you can make all the adjustments to figure size in the .tex file.
	         