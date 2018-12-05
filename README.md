# FIU dissertation using LaTeX

This LaTeX template for the Florida International University (FIU) biology PhD dissertation and MSc thesis adheres to all University graduate school (UGS) rules and guidelines. I have altered files from the FIU Computer Science department, who altered files from Cornell's dissertation template. See the "instructions_README.txt" for additional information.

One important note for professional printing - If you use pdf format figures, not all of the fonts are embedded in the final pdf. If the printer complains about this, run the following line in terminal to embed the missing fonts:

``gs -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -dPDFSETTINGS=/prepress -dEmbedAllFonts=true -sOutputFile=<my_file>_embedded.pdf -f <my_file>.pdf``

where <my_file> is the name of your file and "<my_file>.pdf" is the output from pdflatex
