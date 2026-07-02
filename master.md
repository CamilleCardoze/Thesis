---
title: "Regeneration of a Pharmaceutical Waste Solvent by Batch Extractive Distillation"
author: "Camille Cardoze"
date: 2026
toc: false
numbersections: true
mainfont: "Times New Roman"
sansfont: "Times New Roman"
monofont: "Consolas"
monofontoptions:
  - Scale=0.85
  - Ligatures=TeX
fontsize: 12pt
geometry: "a4paper,margin=1in"
documentclass: report
pdf-engine: xelatex
highlight-style: tango
tables: true
caption-position: below
header-includes:
  - \usepackage{float}
  - \usepackage{graphicx}
  - \usepackage{amsmath}
  - \usepackage{setspace}
  - \usepackage{ragged2e}
  - \numberwithin{equation}{chapter}
  - \usepackage{caption}
  - \captionsetup[table]{font=small}
  - \usepackage{pdfpages}
  - \usepackage{indentfirst}
  - \setlength{\parindent}{1.5em}
  - \addbibresource{refs/library.bib}
  - '\DefineBibliographyStrings{english}{bibliography={References}}'
  - '\defbibheading{bibliography}{\chapter*{\bibname}\addcontentsline{toc}{chapter}{\bibname}}'
biblatexoptions:
  - backend=biber
  - sorting=none

autoEqnLabels: true
filters:
  - pandoc-crossref
---

\pagenumbering{roman}
\setcounter{page}{2}
\pagestyle{plain}

\includepdf[
pages={1},
pagecommand={\thispagestyle{empty}}
]{figs/cover.pdf}
\clearpage

\includepdf[
pages={1},
fitpaper=true,
pagecommand={\thispagestyle{empty}}
]{figs/thesis_sheet.pdf}
\clearpage

\clearpage
\tableofcontents
\addcontentsline{toc}{chapter}{Table of Contents}
\clearpage

\listoffigures
\addcontentsline{toc}{chapter}{List of Figures}
\clearpage

\listoftables
\addcontentsline{toc}{chapter}{List of Tables}
\clearpage

\newpage
