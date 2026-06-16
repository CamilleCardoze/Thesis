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

```{=latex}
\vspace*{2cm}

\begin{center}
{\LARGE\bfseries Declarations}
\end{center}

\vspace{1.65cm}

\begin{center}
Declaration about the acceptability of the thesis
\end{center}

\vspace{0.15cm}

\begin{spacing}{1.02}
This thesis fulfills every formal and content requirements of the regulation of the
Budapest University of Technology and Economics, moreover it fulfills the assignment
of the final project. This thesis is suitable for a review and an open defense.
\end{spacing}

\vspace{0.28cm}

Budapest,

\vspace{2.5cm}

\begin{flushright}
Dr. Hégely László
\end{flushright}

\vspace{2.3cm}

\begin{center}
Declaration about the independent work
\end{center}

\vspace{0.15cm}

\begin{spacing}{1.02}
I, Camille Cardoze (Y3GTYB), hereby declare that the Thesis submitted
for assessment and defense, exclusively contains the results of my own work assisted
by my supervisor. Further to it, it is also stated that all other results taken from the
technical literature or other sources are clearly identified and referred to according to
copyright (footnotes/references are chapter and verse, and placed appropriately).

\vspace{0.22cm}

I accept that the scientific results presented in my Thesis can be utilized by the
Department of the supervisor for further research or teaching purposes.
\end{spacing}

\vspace{0.28cm}

Budapest,

\vspace{2.5cm}

\begin{flushright}
Camille Cardoze
\end{flushright}
```

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
