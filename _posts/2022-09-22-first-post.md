---
layout: post
title:  "An Introduction to $\\LaTeX$"
date:   2022-09-20
author: Noah Lawrence
description: A Guide to $\LaTeX$ (pronounced lay-tech/tek) and how to utilize it efficiently
image: /assets/images/image5.jpg
---
# Introduction
One important skill for Data Scientists is the ability to convey data in a way that is useful for others.  Using tools such as RMarkdown will make creating reports for your data significantly easier.  One of the best tools included in RMarkdown is LaTeX (commonly seen as $\LaTeX$ and pronounced lay-tech/tek), which essentially creates mathematical equations as you would see them in material such as websites and textbooks.  Many of the skills learned in this guide will directly translate to RMarkdown, as the syntax is largely the same. Here, I will make a basic guide to start you on your way to learning LaTeX as well as resources to help you find answers to any questions you have.  It is important to note that I don't know everything about LaTeX and if you find that I missed something, feel free to leave a comment below.

## Installation
There are 2 good starting places for LaTeX on your computer.  First, is an online resource called Overleaf.  It is a free web-based LaTeX editor that can compile your LaTeX code into PDF format for easy reports.  The only downside, in my opinion, is the need to create an account because I don't like having to make an account for every website.

The alternative is to compile LaTeX on your local machine.  For Windows, the most common LaTeX typesetting system is MiKTeX, which comes with a TeX editor called TeXWorks.  For Macintosh, MacTeX is the typesetting system.  For Linux, TeXLive is the most common.  Additionally, there are a variety of editors for each of these platforms, including some that are multiplatform, that you can use to your needs and liking.

Note, this installation will take quite a while because there are such a large number of packages that are included in the base LaTeX installation.  After this installs, you should be able to open your LaTeX editor and begin typing in LaTeX.

For more help on installing for Windows, go <a href="https://miktex.org/howto/install-miktex">here</a>.\
For help installing on MaC, go <a href="https://www.tug.org/mactex/index.html">here</a>.\
For Linux, due to the variety of distributions, I will simply say, Google is your friend here.

## Basic Syntax

LaTeX is a powerful tool to format mathematical formulas in a way that is readable but that isn't its only use.  It can also be used to format documents for reports that are readable and can even include images or charts from tools such as RStudio.  Many academic papers, especially within science and mathematics, are formatted with LaTeX so it is important to learn it.

To create your first document, the following code will be helpful to create it:
> `\documentclass{article}`\
> `\begin{document}`\
> `First document. This is a simple example, with no` \
> `extra parameters or packages included.`\
> `\end{document}`

The first part, `\documentclass{article}` defines the type of document you are creating.  This will call from templates installed on your computer already.  The second part combined with its closing tag is the `\begin{document}` and `\end{document}` is basically the content of your document.  Everything inside of these tags will be what shows up compiled into a PDF.  If any LaTeX code shows up outside of these tags, it will not appear within your PDF.  The following lines are plain text that will be included.  It is important to note that formatting is not included within this part and the fact that the content is on two lines doesn't mean that it will appear that way on the PDF.  To create a new line, you will use the `\\` characters.

One of the most important things in LaTeX is the ability to inline mathematical functions.  For example two-thirds can be represented in Latex as `$\frac{2}{3}$` or $\frac{2}{3}$.  The dollar signs represent inline math functions.  Everything between the two dollar signs will be converted to look like how we most often see it written.  Additionally, there is a math mode that simply uses 2 dollar signs instead of one as is much more useful for long equations.  

Within LaTeX, there are additional functions that allow you greater formatting within your document.  For example, you can create equations using the `\begin{equation}` and `\end{equation}` which will push the equation to the middle of the page.  These are most often called environments and will have specific formatting such as the equation environment shown below.

The PDF of the normal distribution is:
\begin{equation}
\frac{1}{\sigma \sqrt{2\pi}}e^{\frac{-1}{2}(\frac{x-\mu}{\sigma})^2}
\end{equation}

All of these things will need to be included within the document tags to appear in your document.  Since this guide is not by any means exhaustive, I recommend that you try getting the environment setup on your computer and trying out LaTeX for yourself.  Whenever you run into an error, try checking the logs to see where the error was thrown and more often than not, it's missing parenthesis or missing a closing tag for your environments.  When in doubt, Google for the specific error to determine the specific error.  I also recommend visiting Overleaf's documentation and guide, as that will teach much more of the basics and will give you a better idea of the possibilities of LaTeX.  Go on and create your own $\LaTeX$ documents!
## Further Help

<a href="https://www.latex-project.org/help/documentation/usrguide.pdf">LaTeX Documentation</a>\
<a href="https://tex.stackexchange.com/">Tex Stack Overflow</a>\
<a href="https://overleaf.com/">Overleaf</a>\
<a href="https://www.overleaf.com/learn">Overleaf Documentation</a>