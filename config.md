<!--
Add here global page variables to use throughout your website.
-->
+++
author = "Miguel Bustamante"
mintoclevel = 2

prepath = "ssg-blog"

# Add here files or directories that should be ignored by Franklin, otherwise
# these files might be copied and, if markdown, processed by Franklin which
# you might not want. Indicate directories by ending the name with a `/`.
# Base files such as LICENSE.md and README.md are ignored by default.
ignore = ["node_modules/"]

# RSS (the website_{title, descr, url} must be defined to get RSS)
generate_rss = true
website_title = "Miguel Bustamante"
website_descr = "Example website using Franklin"
website_url   = "https://tlienart.github.io/FranklinTemplates.jl/"
+++

<!--
Add here global latex commands to use throughout your pages.
-->
\newcommand{\R}{\mathbb R}
\newcommand{\scal}[1]{\langle #1 \rangle}
\newcommand{\tr}{\textnormal{Tr}}
\newcommand{\grad}{\textnormal{grad}}
\newcommand{\dive}{\textnormal{div}}
\newcommand{\norm}[1]{\left \lVert #1 \right \rVert}
\newcommand{\par}[1]{\left ( #1 \right )}
