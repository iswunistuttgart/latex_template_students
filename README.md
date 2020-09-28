# Thesis template for student thesis at ISW, University of Stuttgart

This template is aimed to provide a LaTeX writing experience with low hurdles.

The template is inspired by [Philipp Tempel's Latex templates](https://github.com/iswunistuttgart/latex-templates) with a focus on minimum dependencies and low user entry level.

## How to use it:

1. Set up the project
   1. Search for ISW student thesis template on [Overleaf](https://www.overleaf.com/latex/templates/isw-student-thesis/xjwkfntnwrwc), then start your project from there. This is the prefered method. No Latex installation, no package problems, just write.
   2. Or get it from this repository.
      - You need LaTeX installed on your operating system
      - Compile it with Lualatex [recommended] or pdflatex
2. Select the main file you need
   - Exposé? --> `Name_Expose.tex` (+ `iswthesis.sty`)
   - Thesis?
     - Want to setup your own? --> `Name_Thema_min.tex` (+ `iswthesis.sty`)
     - Nees suggestions which packages to use? -> `Name_Thema.tex` (+ the whole directory)
3. Start

## Directory structure

```sh
.
├── bibliography.bib    # demo bibliography. replace with your own.
├── chapters            # place your chapters here
│   ├── Acronyms.tex    # definition of acronyms
│   ├── Einleitung.tex  # sample chapter
│   └── Examples.tex    # examples, how-to introduction
├── example_figures/    # figures used in examples
├── images/             # logo sources
├── iswthesis.sty       # the ISW styling class
├── Name_Exposee.tex    # sample exposé, start from here when you are writing one.
├── Name_Thema.tex      # sample thesis with packages you might find useful
├── Name_Thema_min.tex  # minimal sample thesis. Load your own packages
├── README.md
└── settings.tex        # settings file used in the sample thesis document

```

### `iswthesis.sty`

Simplifying thesis writing in LaTeX complying with the style of ISW, University of Stuttgart.

This class does the styling for you (together with a komascript class).

It handles the following:

- Proper input and font encoding (Just type, don't care about the LaTeX compiler you use or how to type German umlauts)
- Fonts with ligatures and kerning (Tex Gyre fonts are used, part of every LaTeX installation, text is nice to read)
- Bibliography styling for biblatex (declare your bibliography file and you are ready to go)
- Provide command for title page (`\makeISWtitle`) and declaration of originality ( `\declarationOfOriginality`)
- Loads packages "biblatex" and "graphics"

We tried to minimize the package dependencies. This is a styling package, not a documentclass. Komascript does the rest.
Below is a list of the packages we need to load anyhow.

| Packages                                                        | Why                                     |
| --------------------------------------------------------------- | --------------------------------------- |
| `ifthen`, `ifpdf`, `ifxetex`, `ifluatex`, `iflang`, `kvoptions` | Options handling                        |
| `microtype`                                                     | font kerning                            |
| [just pdflatex] `fontenc`, `inputenc`                           | handle encodings                        |
|                                                                 | sans serif font for headings            |
| [just luatex and xetex] `fontspec`                              | fonts loading                           |
| `mathpazo`, `tgpagella`, `tgheros` , `DejaVuSansMono` `textcomp`| fonts                                   |
| `csquotes`                                                      | handling quotes correctly with biblatex |
| `biblatex`                                                      | bibliography                            |
| `graphicx`                                                      | loading logo image for the titlepage    |


