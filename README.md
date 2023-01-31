# UniMelb_classicthesis

A LaTeX template based on [classicthesis](https://ctan.org/pkg/classicthesis) and modified for University of Melbourne research degrees.

If this template is being used for a UniMelb PhD or Master by Research thesis, the [Preparation of Graduate Research Theses Rules](https://gradresearch.unimelb.edu.au/preparing-my-thesis/preparation-of-graduate-research-theses-rules) MUST be followed. Some available customisations and important rules are listed below.

## Requirements

LaTeX and [classicthesis](https://ctan.org/pkg/classicthesis) package, which is included in [TeXLive](https://www.tug.org/texlive/).

## Usage

To insert a chapter, say `Chapter A`, do the following:
 1. Create `Chapters\A` folder. This is where the `tex` file(s) goes.
 2. Create `Figures\A` folder. This is where the figures for this chapter go.
 3. Create `Chapters\A\A.tex` file, write `\graphicspath{{Figures/A}}` as the first line to configure the path of figures. When inserting a figure, only use the filename without its path.

## University of Melbourne thesis rules

 - The guidelines for some required contents (e.g., Preface) are already included in the template.
 - The UniMelb logo CANNOT appear in the thesis.
 - The margins of both sides should be at least 3 cm (already implemented in this template).
 - The thesis title should be sentence-case, DO NOT uncomment the `\spacedallcaps` line in [Titlepage.tex](FrontBackmatter/Titlepage.tex). A sample title page can be found [here](https://gradresearch.unimelb.edu.au/__data/assets/word_doc/0004/3183511/Sample_Thesis-title-page_18Jul22.docx), which is followed by this template.
 - An OrcID MUST be included, which can be inserted in [classicthesis-config.tex](classicthesis-config.tex) along with other author information. The link of the OrcID needs to be manually changed in [Titlepage.tex](FrontBackmatter/Titlepage.tex).

## Customisations

 - Thesis, author and supervisor information can be inserted in [classicthesis-config.tex](classicthesis-config.tex), stick with sentence-case.
 - [Dedication](FrontBackmatter/Dedication.tex) is optional and can be commented in [main.tex](main.tex).
 - An author signature should be inserted in [Declaration](FrontBackmatter/Declaration.tex) where it is currently commented.
 - [newcommands.tex](Preamble/newcommands.tex) contains some custom commands for mathematical symbols. It is optional and can be removed at the end of [classicthesis-config.tex](classicthesis-config.tex).
 - The colours of text and links are changed to `RoyalBlue` for a UniMelb style, they can be modified or removed at the end of [classicthesis-config.tex](classicthesis-config.tex).
 - Citations are handled by `biblatex` and are in `APA 7th` style. This can be changed in [packages.tex](Preamble/packages.tex).
 - Some common options (e.g., math font, text font, numbering per chapter) can be modified in the first part of [classicthesis-config.tex](classicthesis-config.tex).
 - Template is set to `twoside` by default in `\documentclass` in [main.tex](main.tex), which refers to two-sided book style. That means the content on each page will appear towards the left or right for odd and even pages, respectively, and if a chapter ends on an odd page, and empty page will be inserted. If you do not like this, change `twoside` to `oneside`.
 - Parts (one level higher than chapters) and Appendix can be turned on or off in [main.tex](main.tex).
 - The table of contents currently includes List of Figures, List of Tables, Listings and Acronyms. If you would like to remove any of them, comment the corresponding lines in [Contents.tex](FrontBackmatter/Contents.tex).
 - Front matters (Dedication, Abstract, Declaration, Preface and Acknowledgements) are included in the table of contents. To remove any of them, comment the `\phantomsection` and `\addcontentsline` lines in the `tex` file.