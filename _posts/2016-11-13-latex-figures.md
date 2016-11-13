---
title: How to include LaTeX fonts in figures
updated: 2016-03-20 21:56
---

There are multiple tools that can be used in order to draw figures to be included in a LaTeX document like [ipe](http://ipe.otfried.org/) or [LaTeXDraw](http://latexdraw.sourceforge.net/). Despite that most of these tools can incorporate LaTeX code into the figure, they ignore the configuration of your document, like the fonts, font size etc. Furthermore, I do not like to be restricted from one editor in order to draw a figure for LaTeX documents as I have figures produced by different editors. In general, I like to use a generic editor for most of my drawings, like [Inkscape](https://inkscape.org/en/).

For this purpose, I find useful the [psfrag](https://www.ctan.org/pkg/psfrag?lang=en) package with which someone can replace the text within an EPS figure with LaTeX code:

```latex
\begin{figure}[!t]
  \centering
  \psfrag{hs}{$h_s$}
  \psfrag{hn}{$\hat{h}_n$}
  \includegraphics{fig.eps}%
\end{figure}
```

This way you can include an EPS file that has been produced by any arbirtrary editor inside your LaTeX document. However, the limitation of this package is that you have to use `latex` and not `pdflatex` for your documents. If your document is heavily depended on `pdflatex` (e.g. it uses packages that work only with `pdflatex`) a solution is to produce a PDF output of the figure outside your document and then to include it in your document.

In my workflow I use a bash script similar to this for producing the document:

```bash
latex main.tex && \
dvips main.dvi && \
ps2pdf main.ps && \
gnome-open main.pdf
```
