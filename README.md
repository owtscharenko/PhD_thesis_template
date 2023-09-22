# PhD thesis template

This is a latex template for writing a PhD (or masters) thesis.
The project uses numerous latex packages, so a full latex install is recommended.  
The project uses biber with a customized bibstyle for the bibliography and glossaries-extra for the glossary. For a full compilation following recipe is used:
1. pdflatex
2. bibtex
3. mageglossaries
4. pdflatex
5. pdflatex

For an editor I can recommend VS code with the [Latex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension and the [LTeX - Language tool](https://marketplace.visualstudio.com/items?itemName=valentjn.vscode-ltex). The vs code settings file is part of this repository.  
The [jabref](https://jabref.org) bibliography tool can output a .bib file which can directly be used by biber.

In the root directory there is the **main.tex** file, the bibliography and the glossary files.  
In this file include directories **chapter** for the single thesis chapters and **figures** for figures to include in the thesis are defined.  
The thesis title is defined in [L. 252](https://git.hep.physik.uni-siegen.de/latex/phd-thesis-template/-/blob/main/Main.tex?ref_type=heads#L252).  
On the second page the referees and the date of oral examination have to be printed, this is defined in [L. 275](https://git.hep.physik.uni-siegen.de/latex/phd-thesis-template/-/blob/main/Main.tex?ref_type=heads#L275).

The **siunitx** package introduces proper display of numbers and values with uncertainties and units. You can even define your own units (see [L. 165](https://git.hep.physik.uni-siegen.de/latex/phd-thesis-template/-/blob/main/Main.tex?ref_type=heads#L165) ff in main.tex).

The **cleverref** package automatically prints the correct designator in front of the identifier of the object you refer to. E. g. "Figure" in front of the figure you reference. An example is shown in [L. 64 of chapter/Example_chapter.tex](https://git.hep.physik.uni-siegen.de/latex/phd-thesis-template/-/blob/main/chapter/Example_chapter.tex?ref_type=heads#L64).

The color of hyperlinks in the text is defined in [L. 192](https://git.hep.physik.uni-siegen.de/latex/phd-thesis-template/-/blob/main/Main.tex?ref_type=heads#L192) ff. It is recommended by the Library team to turn off colored links in the printed version of the PhD thesis.

The pdf version for the Siegen library needs to have all fonts embedded but can not contain any *Type3* fonts. This means you have to modify the pdf document with Adobe acrobat pro as explained [here](https://github.com/matplotlib/matplotlib/issues/21797#issuecomment-999403223). At the time of wrting, [Adobe acrobat pro is available for employees of University of Siegen free of charge](https://www.zimt.uni-siegen.de/beratung_und_lehre/software/adobe/adobe-etla-cc.html?lang=de).

In case you do plots with **MATPLOTLIB** be aware that any greek letters will be from the font DejaVuSans-Oblique, which will not be embedded in the pdf by matplotlib. Instead the greek letters will be rendered from vector paths. There is no displaying issue, but the library needs all mentioned fonts embedded in the pdf. If you follow the discussion under the link above this can be resolved with the preflight tool. 