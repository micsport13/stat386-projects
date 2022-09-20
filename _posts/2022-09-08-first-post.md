---
layout: post
title:  "First Post"
date:   2022-09-20
author: Noah Lawrence
description: A Guide to $\LaTeX$
image: /assets/images/image5.jpg
---
One important skill for Data Scientists is the ability to convey data in a way that is useful for others.  Using tools such as RMarkdown will make creating reports for your data significantly easier.  One of the best tools included in RMarkdown is LaTeX (commonly seen as $\LaTeX$), which essentially creates mathematical equations as you would see them in material such as websites and textbooks.  Here, I will make a basic guide to start you on your way to learning LaTeX as well as resources to help you find answers to any questions you have.  It is important to note that I don't know everything about LaTeX and if you find that I missed something, feel free to leave a comment below.



# Installation
There are 2 good starting places for LaTeX on your computer.  First, is an online resource called Overleaf.  It is a free web-based LaTeX editor that simply

# Basic Syntax
One of the most important things in LaTeX (pronounced lay-tech/tek) is the ability to inline mathematical functions.  For example two-thirds can be represented in Latex as `$\frac{2}{3}$` or $\frac{2}{3}$.  The dollar signs represent inline math functions.  Everything between the two dollar signs will be converted to look like how we most often see it written.  Additionally, there is a math mode that simply uses 2 dollar signs instead of one as is much more useful for long equations.  

Within LaTeX, there are additional functions that allow you greater formatting within your document.  For example, you can create equations using the `\begin{equation}` and `\end{equation}` which will push the equation to the middle of the page. 

The PMF of the normal distribution is:
\begin{equation}
\frac{1}{\sigma \sqrt{2\pi}}e^{\frac{-1}{2}\frac{x-\mu}{\sigma}^2}
\end{equation}

LaTeX is a powerful tool to format mathematical formulas in a way that is readable

# Further Help

<a href="https://www.latex-project.org/help/documentation/usrguide.pdf">LaTeX Documentation