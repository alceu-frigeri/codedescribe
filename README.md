
codedescribe / codelisting
==========

These are expl3 based packages for LaTeX/expl3 code documetation.
### codedescribe
 provides a series of macros/environments (similar to doc/docx/doc3) for package/classes documentantion
### codelisting
 provides a few macros for LaTeX code listing/demo.

They are designed to be 'as class independent as possible',
no assumption about underline macros is made.
Furthermore, it's assumed that *\maketitle* and the *abstract* environment
were modified by the underline class, so alternatives (based on the article class) are provided.

For more details,  see the documentation,
[codedescribe.pdf](http://mirrors.ctan.org/macros/latex/contrib/codedescribe/doc/codedescribe.pdf)

--------------

## Requirements
* none besides a fairly recent LaTeX distribution as recent as 2022/06/01
(with the new in kernel *\ProcessKeyOptions* and *\NewDocumentCommand*)

## Installation
The stable version is available at [CTAN](https://ctan.org/pkg/codedescribe).

## Usage
### Stable version
Just place
```latex
  \usepackage{codedescribe}
```

in the preamble and compile away.


Be aware that options might change between versions, so you have to check them manually.

## More Information and documentation
More Information can be found in the documentation; you can find a  "bleeding edge" version
at [the github page](http://github.com/alceu-frigeri/codedescribe)

## Contacting Author

For bug reports and enhacement suggestions, the preferred way is to use
[the project's issue page](https://github.com/alceu-frigeri/codedescribe/issues).
Please be ready to provide an example code showing the bug, if any.

Please do not use the issue page for generic help on how to use the package.

* git: https://github.com/alceu-frigeri/codedescribe

-------------
Copyright 2023-present by Alceu Frigeri

 This work may be distributed and/or modified under the
 conditions of

 * The [LaTeX Project Public License](http://www.latex-project.org/lppl.txt), version 1.3c (or later), and/or
 * The [GNU Affero General Public License](https://www.gnu.org/licenses/agpl-3.0.html), version 3 (or later)

This work has the LPPL maintenance status *maintained*.

The Current Maintainer of this work is Alceu Frigeri

-------------
## This work consists of the files

* codelisting.sty
    - set of macros to typeset and demonstrate LaTeX code

* codedescribe.sty
    - set of macros to document LaTeX packages

* README.md (this file)
    - quick introduction

* codedescribe.tex
    - package documentation

* codedescribe.pdf
    - documentation in PDF format

-------------

## Changelog

* Version 1.5 (this)
    - fixing #1 (wrong spacing when missing a `codesyntax` inner environment. 

* Version 1.4
    - The 'new', 'update' and 'info' keys can, now, be used multiple times when declaring a codedescribe environment. (see documentation).

* Version 1.3
    - Added \tsresult, a command to just show the result of a stored code (codelisting specific).


* Version 1.2
    - Added format key: basicstyle
    
* Version 1.1
    - Added two commands to allow <obj-types> customization 
    - requiring (now) pifont for EXP/rEXP <format-keys>
    - Added a date command (auxiliary command)

* Version 1.0 
    - Initial release by CTAN
