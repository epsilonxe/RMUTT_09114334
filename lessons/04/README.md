# Logical structure

<span
  class="summary">This lesson shows some basic formatting commands, and compares them with semantic formatting with sectioning commands and lists.</span>

LaTeX provides ways to concentrate on the logical structure of your document, as well as the
ability to directly set the appearance. Most of the time, it's much better to use
methods that focus on structure, as that makes it easy to reuse or alter
appearance when you have to.

## Structure and visual presentation

We'll start with an example contrasting one of the most common logical markup
commands in LaTeX, `\emph`, with simply making something italic. (In print,
that's usually how things are emphasized.)

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}
Some text with \emph{emphasis and \emph{nested} content}.

Some text in \textit{italic and \textit{nested} content}.
\end{document}
```

You can probably guess that `\textit` is a command to make text italic, but it
_always_ makes things italic, so it doesn't work for nested material. See how
`\emph` _does_ know about nesting. There are also places where the emphasis
isn't the same as italic; for example, in presentations color is usually a better
option. With logical markup, we don't have to worry about that detail in the
body of the document.

We will look at manual formatting later, but for the moment we'll
add `\textbf` to commands we know: it makes text bold.

## Sectioning commands

You probably have used a word processor, where  to start a section most people
enter the title text then simply make it bigger and bold, and follow it with a
new line. In LaTeX, using logical markup is actually _easier_ than doing the
formatting by hand; we can use the `\section` command. This handles the font
changes, vertical space, etc., and keeps the output uniform throughout the
document.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}
Hey world!

This is a first document.

\section{Title of the first section}

Text of material in the first section

Second paragraph.

\subsection{Subsection of the first section}

Text of material in the subsection.

\section{Second section}

Text of the second section.

\end{document}
```

Using the standard `article` setup, LaTeX numbers the sections and subsections
and includes the titles in boldface. We'll think a bit about changing design [in
the next lesson](lesson-05).

LaTeX can divide up documents into quite a few levels

- `\chapter` (but we need `\documentclass{book}` or
  `\documentclass{report}` for this)
- `\section`
- `\subsection`
- `\subsubsection`

We can go further: the next one 'down' is `\paragraph`, but almost always that's
too much 'detail' in sections. (Yes, `\paragraph` is a section command, _not_ a
way to start a new paragraph!)

You might wonder about the title of a document. There are some special
commands for that, but not all documents use them, so we've
covered that in the parallel extra lesson.

## Lists

The other very common place you'll want logical markup is writing lists.
There are two common types of list built in to LaTeX.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}

Ordered
\begin{enumerate}
  \item An entry
  \item Another One
  \item Wow! Three entries
\end{enumerate}

Unordered
\begin{itemize}
  \item An entry
  \item Another One
  \item Wow! Three entries
\end{itemize}

\end{document}
```

Notice that we use `\item` to start each entry, and that the marker used  for
each type of list is added automatically.

---

"More on: Logical structure"


## Document titles

LaTeX offers some logical markup for the title of documents: three commands
to set up 'meta-data' and one to use it.

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}
\author{A.~N.~Other \and D.~Nobacon}
\title{Some things I did}
\date{1st April 2020}
\maketitle

Some normal text.
\end{document}
```

As you can see, the commands `\author`, `\title` and `\date` save information,
and `\maketitle` uses it. You can also separate multiple authors with `\and`.
The commands `\author`, `\title` and `\date` need to come before `\maketitle`.
Here, we've given them in the document body: they can also be used in the
preamble, but if you use `babel` shortcuts they won't be active there.

The design provided by `\maketitle` depends on the document class (see [lesson
5](lesson-05)). There is a `titlepage` environment for when you want to do
custom design, but this is out of the scope of this introduction.  If you want
to do your own document designs you can either use a customisable class, such
as `memoir`, or start with one of LaTeX's base classes, like `book` and use it
as a starting point.

## Descriptive lists
In addition to the "ordered" and "unordered" types of lists, LaTeX provides
another one, less common: the "descriptive lists".

```latex
\documentclass{article}
\usepackage[T1]{fontenc}
\begin{document}

\begin{description}
\item[Dog:] member of the genus Canis, which forms part of the wolf-like canids,
  and is the most widely abundant terrestrial carnivore.
\item[Cat:] domestic species of small carnivorous mammal. It is the only
  domesticated species in the family Felidae and is often referred to as the
  domestic cat to distinguish it from the wild members of the family.
\end{description}

\end{document}
```


## Exercise 1

Experiment with different sectioning levels. Try using `\documentclass{report}`
instead of `\documentclass{article}` and adding `\chapter` commands. How
do they look? Try out `\paragraph` and (even) `\subparagraph` to see they work:
by default, they _don't_ add numbers.

Make some lists, and nest one list inside another. How does the format of the
numbers or markers change? You can only go to four levels with standard LaTeX,
but more than four nested lists tends to be a bad sign anyway!

## Exercise 2

Try setting up different `\author`, `\title` and `\date` information to test
out `\maketitle`. Which of them do you _have_ to give? Do the commands have to
have an author, a title and a date in them?

Make some descriptive lists, and nest some of them inside another ones (ordered,
unordered or descriptive).


