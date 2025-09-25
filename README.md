
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
* codedescribe.bib
    - package documentation

* codedescribe.pdf
    - documentation in PDF format

-------------

## Changelog

* Version 1.12 (this)
  - Documentation typos and some clarification regardings packages errors/warnings.
  - \describe macro defined only inside a describelist environment.
  - Package option added: strict (warnings will be redirect as package errors)
  

* Version 1.11
  - replacing \vspace with \skip_vertical:n
  - peeking ahead \ts* commands (for further spacing fine tune).
  - using xpeekahead for the peek ahead part.
  - added a package option: color scheme (see documentation).
  - documentation (specially due to kernel changes regarding key handlers).

* Version 1.10
  - fixing [#10](https://github.com/alceu-frigeri/codedescribe/issues/10) (hopefully for good) by implementing [env-peekahead](https://tex.stackexchange.com/questions/745593/peek-ahead-in-expl3) and [skip-spacing](https://tex.stackexchange.com/questions/745692/inter-coffins-spacing)
  - environments code cleanup.
  - spacing fine tuning
  - deprecating tsremark* (should't exist!)
  - implementing [#11](https://github.com/alceu-frigeri/codedescribe/issues/11)

* Version 1.9
    - added two keys (letter and other) to Code Keys (see manual)
    - setting, by default, _:@ as letters (for expl3) [#9](https://github.com/alceu-frigeri/codedescribe/issues/9)
    - added a few option keys to further customize \tsobj (bnf style lists, see manual)
    - documentation review (typos, clarity).
    - code cleanup.

* Version 1.8
    - fixes
      [#6](https://github.com/alceu-frigeri/codedescribe/issues/6), [#7](https://github.com/alceu-frigeri/codedescribe/issues/7) and
      [#8](https://github.com/alceu-frigeri/codedescribe/issues/7).
    - Added an (optional) index parameter to the code display/demo commands.
    - New command: \tsmergedcode, \tsexec and \setnewcodekey (see documentation).


* Version 1.7
    - fixing  [#4](https://github.com/alceu-frigeri/codedescribe/issues/4) (hopefully) for good and working on [#5](https://github.com/alceu-frigeri/codedescribe/issues/5). Added an environment <tsremark*> (see documentation). 

* Version 1.6
    - fixing issue [#3](https://github.com/alceu-frigeri/codedescribe/issues/3) (long standing (hidden) bug. \tsresult now fully respects optional keys.

* Version 1.5b 
    - fixing issue [#2](https://github.com/alceu-frigeri/codedescribe/issues/2) (reverting `codesyntax` bug introduced by v1.5). 

* Version 1.5
    - fixing issue [#1](https://github.com/alceu-frigeri/codedescribe/issues/1) (misalignment when missing a `codesyntax` inner environment). 

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
