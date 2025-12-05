# Getting Started with LaTeX

## 2\. The Basic Document Structure

Every LaTeX document must have a preamble and a document body. The file extension is typically `.tex`.

```latex
\documentclass[10pt, a4paper]{article} 
\usepackage{amsmath} % Example of a package for math

\title{My First LaTeX Document}
\author{A Helpful AI Assistant}
\date{\today}

\begin{document}

\maketitle % Prints the title, author, and date

\section{Introduction} 
This is the main text of my document. A blank line separates paragraphs.
LaTeX is great for typesetting.

\subsection{Basic Text Formatting}
Use \textbf{bold text}, \textit{italic text}, and \underline{underlined text}.

\section{The End} 
All content goes inside the document environment.

\end{document}
```

-----

## Key Concepts and Commands

### A. Document Class (`\documentclass`)

This command defines the overall structure of your document. It must be the *first* command in your file.

| Class | Purpose |
| :--- | :--- |
| `article` | Short reports, papers, and articles. |
| `report` | Longer documents with chapters, like theses. |
| `book` | Books and very long documents. |
| `letter` | Writing letters. |

**Options** (in square brackets `[]`): Common options include font size (`10pt`, `11pt`, `12pt`) and paper size (`a4paper`, `letterpaper`). Example: `\documentclass[12pt, letterpaper]{article}`.

### B. Packages (`\usepackage`)

Packages extend LaTeX's functionality. They are placed in the **preamble** (before `\begin{document}`).

| Package | Purpose |
| :--- | :--- |
| `amsmath` | Essential for complex mathematical typesetting. |
| `graphicx` | For including images. |
| `hyperref` | For creating hyperlinks in the PDF. |
| `geometry` | To easily customize page margins. |

### C. Structure and Headings

LaTeX uses commands to define the logical structure of your document, which automatically handles numbering and formatting.

  * `\section{Section Title}`
  * `\subsection{Subsection Title}`
  * `\subsubsection{Sub-subsection Title}`
  * For `report` or `book` class: `\chapter{Chapter Title}`

### D. Comments

Use the percent sign (`%`) to add comments. Everything from the `%` to the end of the line is ignored by the compiler.

```latex
This is normal text. % This is a comment and will not appear in the output.
```

-----

## Typesetting Mathematics

One of LaTeX's greatest strengths is its ability to typeset complex mathematical equations beautifully.

### 1\. Inline Math

To include a short formula *within* a line of text, wrap it in dollar signs (`$`).

| LaTeX Code | Output |
| :--- | :--- |
| `The function is $f(x) = x^2 + 2x + 1$.` | The function is $f(x) = x^2 + 2x + 1$. |

### 2\. Displayed Math (Numbered)

For equations you want centered on their own line and automatically numbered, use the `equation` environment:

```latex
\begin{equation}
E = mc^2
\label{eq:einstein} 
\end{equation}
```

$$E = mc^2$$

### 3\. Key Math Commands

| Command | Output | Purpose |
| :--- | :--- | :--- |
| `^` | $x^2$ | Superscript (e.g., $x^2$) |
| `_` | $x_i$ | Subscript (e.g., $x_i$) |
| `\frac{a}{b}` | $\frac{a}{b}$ | Fractions |
| `\sqrt{x}` | $\sqrt{x}$ | Square root |
| `\sum_{i=0}^{\infty}` | $\sum_{i=0}^{\infty}$ | Summation (limits below/above) |
| `\alpha`, `\beta`, `\Omega` | $\alpha, \beta, \Omega$ | Greek letters |
| `\int_a^b` | $\int_a^b$ | Integrals |

-----

## Lists, Tables, and Images

### 1\. Lists

  * **Unordered List (Bullet Points):** Use the `itemize` environment.
  * **Ordered List (Numbered):** Use the `enumerate` environment.

<!-- end list -->

```latex
\begin{itemize}
    \item First item.
    \item Second item.
\end{itemize}
```

### 2\. Including Images

You must use the `graphicx` package for this. The code is placed inside a **figure environment** to make the image a *float*, allowing LaTeX to position it optimally.

```latex
\begin{figure}[h] % [h] suggests "here"
    \centering
    \includegraphics[width=0.8\textwidth]{my_image_file.png} 
    \caption{This is a caption for my figure.}
    \label{fig:example}
\end{figure}
```

### 3\. Referencing

You can cross-reference sections, equations, figures, and tables using `\label` and `\ref`.

1.  Place a `\label{key}` command immediately after the title/caption command.
2.  Use `\ref{key}` to reference the number. (e.g., "As seen in Figure \\ref{fig:example}...")

-----

## Best Practices and Resources

  * **Compilation:** You need to *compile* your `.tex` file into a PDF. In online editors, this is usually a "Recompile" or "Build" button. Sometimes, for references to work correctly, you may need to compile twice.
  * **The Not So Short Introduction to LaTeX:** This is the classic, comprehensive, and free PDF guide to learning LaTeX.
  * **Overleaf Documentation:** Overleaf provides excellent, bite-sized tutorials and help pages for specific tasks.
  * **CTAN (Comprehensive TeX Archive Network):** This is the central repository for all LaTeX packages, classes, and documentation.

Would you like to try writing a small sample document with a math equation, and I can walk you through the LaTeX code?