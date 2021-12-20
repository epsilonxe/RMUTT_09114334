# LaTeX basics

<span
  class="summary">This lesson explains the basics of what LaTeX is and how it works in contrast to common word processors such as Microsoft Word or LibreOffice Writer.</span>

Unlike common word processors such as Microsoft Word or LibreOffice Writer, LaTeX
usually does not provide WYSIWYG ('What You See Is What You Get'). With LaTeX
one takes plain text and enriches it with markup. This markup tells LaTeX
about the logical meaning of certain elements of the text, similar to the way
HTML does.

Take for example the element `<h2>` indicating a new section in an HTML document.
LaTeX also has a command for this; here one would use the `\section` command.

## The LaTeX workflow

Because LaTeX files are not the document itself but rather instructions
on what each part of the document should be, you don't normally give other
people your LaTeX file itself. Instead, after writing your LaTeX _source_, you
run LaTeX on the file (normally using a program called `pdflatex`) to
create a PDF file. This PDF is then what you send to others.

Different people use different ways to describe this process. As using LaTeX
is a bit like programming, it's often called 'compiling' your document, although
'typesetting' is more accurate.

## Multiple LaTeX runs

For simple files, you only need to typeset your file once to get the completed
PDF. But once you start adding more complicated things, like cross-references,
citations, figures, and tables of contents, you might need to run LaTeX more
than once. We'll tell you when that's the case.

## LaTeX or pdfLaTeX or ...

In the [next lesson](lesson-02), we are going to see that LaTeX is not a
single program. To keep things simple, we are going to focus on one particular
LaTeX Program, pdfLaTeX, for creating your PDFs. We will look at some other
programs, and why you might want to use them, later in the course.


# More on: What is LaTeX and how does it work?

The word 'LaTeX' actually consists of two components, 'La' and 'TeX'. In the
following we will briefly describe where they come from.

TeX was originally invented by Stanford professor Donald Knuth. Knuth is
well known for a series of books called *The Art of Computer Programming*
(known as TAOCP). In
1973 a new edition of the books was to be made; this was the time when the
typesetting industry switched from traditional typesetting with lead to
photo-based typesetting. Donald Knuth did not like the quality of the print and
therefore decided to implement his own typesetting system.

In May 1977 the development of TeX started.

The original TeX was rather complicated to use, even Donald Knuth used various
macros to edit his books. Leslie Lamport, who works for Microsoft nowadays, also
developed a set of macros that simplify the use of TeX and called this macro
set “LaTeX”.

Today LaTeX is the most common way to interact with TeX. Another alternative is
[ConTeXt](https://www.contextgarden.net/).