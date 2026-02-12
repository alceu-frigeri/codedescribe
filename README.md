
codedescribe / codelisting
==========

These are expl3 based packages for LaTeX/expl3 code documetation.
### codedescribe
 provides a series of macros/environments (similar to doc/docx/doc3) for package/classes documentantion
### codelisting
 provides a few macros for LaTeX code listing/demo.

They are designed to be 'as class independent as possible',
no assumption about underlying macros is made.
Furthermore, it's assumed that *\maketitle* and the *abstract* environment
were modified by the underlying class, so alternatives (based on the article class) are provided.

For more details,  see the documentation,
[codedescribe.pdf](http://mirrors.ctan.org/macros/latex/contrib/codedescribe/doc/codedescribe.pdf)

--------------

## Requirements
* none besides a fairly recent LaTeX distribution as recent as [2025/06/01](https://ctan.org/pkg/l3kernel)
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

For help on how to use the package, suggestions, use
[the project's discussion page](https://github.com/alceu-frigeri/codedescribe/discussions).

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

### This work consists of the files

* codelisting.sty
    - set of macros to typeset and demonstrate LaTeX code

* codedescribe.sty
    - set of macros to document LaTeX packages

* codedescsets.sty
    - sets of locale definitions

* codelstlang.sty
    - sets of listings dialect/language definitions

* codecmm.sty
    - a few auxiliary commands (mostly skip/dim related)

* README.md (this file)
    - quick introduction

* codedescribe.tex
* codedescribe.bib
    - package documentation

* codedescribe.pdf
    - documentation in PDF format

-------------

### Change log

* Version 1.24 (this)
  - added a shortcut for `\tsmacro` as well
  - ditched the global bool (force margin) from codedescribe environment.
  - added 'faint' color (for code variants)
  - added 'variants' key (helper for typesetting expl commands)
  - fixing [\#36](https://github.com/alceu-frigeri/codedescribe/issues/36)
  
* Version 1.23
  - codelist partial refaktor: code is more regular, systematic now, regarding listings. 
    some keys got deprecated.
  - shortcuts: making `!` active, supporting `\tsobj`, `\tsargs`, `\tsverb`, `\tsmeta` and `\tsmarginnote`

* Version 1.22
  - documentation typos.
  - \setnewcodekey deprecated in favour of \newcodekey.
  - \selectlabelset deprecated in favour of \setcodelabels
  - fixing readme markdown compatibility issues between github and ctan...
  - new auxiliary command \indexgenkey and related keys `index gen group` and `index gen prefix`
  

* Version 1.21
  - fixing [\#26](https://github.com/alceu-frigeri/codedescribe/issues/26), long standing hidden bug.
  - add `codesyntax*` environment (verbatim alternative, [\#27](https://github.com/alceu-frigeri/codedescribe/issues/27))
  - adjusted (optimized) the (re)definition of `verbatimsc` environment [\#28](https://github.com/alceu-frigeri/codedescribe/issues/28)
  - extended index generating support, keys and `\indexcodesetup` (related to [\#25](https://github.com/alceu-frigeri/codedescribe/issues/25))
  - added a series of index generating auxiliary commands
  - whole index coding depends on global package option index (reducing the overhead when it isn't needed)

* Version 1.20
  - new format keys to adjust spacing in \tsobj and margin block placement in `codedescribe` environment 
    (addressing [\#23](https://github.com/alceu-frigeri/codedescribe/issues/23) and 
    [\#24](https://github.com/alceu-frigeri/codedescribe/issues/24))
  - new command to copy/duplicate a group format.
  - new setup to help making an index [\#25](https://github.com/alceu-frigeri/codedescribe/issues/25)
  - new commands for color customization (both codedescribe and codelisting as well)
  - added a listings' key, firstnumber (codelisting, \tscode and related)
  - codedescribe package options regarding changes above.
  - documentation review.
    
* Version 1.19
  - codesyntax new optional parameter, addressing [\#21](https://github.com/alceu-frigeri/codedescribe/issues/21) 
  - new format keys (font and fsize), addressing [\#22](https://github.com/alceu-frigeri/codedescribe/issues/22)
  - code demo logic reworked,  addressing [\#20](https://github.com/alceu-frigeri/codedescribe/issues/20)
  - new auxiliary package codecmm, to hold those few commands shared between codedescribe and codelisting making them independent from each other.
    
* Version 1.18
  - new commands and package option for label sets ('locale') 
  - addressing [\#17](https://github.com/alceu-frigeri/codedescribe/issues/17) 
  - partially addressing [\#18](https://github.com/alceu-frigeri/codedescribe/issues/18) in the documentation
  - new package option to suppress some annoying bad boxes warnings.

* Version 1.17
  - using ```\pkginfograbProvidesExplPackage```
  - New auxiliary package codelstlang.sty (defines a series of listings TeX dialects). 
  - New package options to set which TeX dialect(s) to be used. 
  - New code key: `lststyle` to use a listings' user defined style, instead of the provided one.

* Version 1.16b 
  - fixing [\#15](https://github.com/alceu-frigeri/codedescribe/issues/15) (codesyntax snafu, introduced by last update)

* Version 1.16a
  - code cleanup (better following expl3 convention) and a bit of optimization.


* Version 1.16
  - removing references to expl scratch variables, like `\l_tmpa_tl` and `\l_tmpa_int`.
  - using `pkginfograb`


* Version 1.15
  - pre-compiling regex
  - removing llongblock bool ...
  - [\#14](https://github.com/alceu-frigeri/codedescribe/issues/14) (typo... in code)

* Version 1.14 
  - footnote work around for hyperref (addressing issue [\#13](https://github.com/alceu-frigeri/codedescribe/issues/13))
  - documentation.


* Version 1.13
  - codedescribe/codesyntax/text interaction fine tuning (in longblock case)
  - removing "spurious code" (ancient leftover code).


* Version 1.12 
  - Documentation typos and some clarification regarding packages errors/warnings.
  - \describe macro defined only inside a describelist environment.
  - Package option added: strict (warnings will be redirected as package errors)
  

* Version 1.11
  - replacing \vspace with \skip_vertical:n
  - peeking ahead \ts* commands (for further spacing fine tune).
  - using xpeekahead for the peek ahead part.
  - added a package option: color scheme (see documentation).
  - documentation (specially due to kernel changes regarding key handlers).

* Version 1.10
  - fixing [\#10](https://github.com/alceu-frigeri/codedescribe/issues/10) (hopefully for good) by implementing 
    [env-peekahead](https://tex.stackexchange.com/questions/745593/peek-ahead-in-expl3) and 
    [skip-spacing](https://tex.stackexchange.com/questions/745692/inter-coffins-spacing)
  - environments code cleanup.
  - spacing fine tuning
  - deprecating tsremark* (should't exist!)
  - implementing [\#11](https://github.com/alceu-frigeri/codedescribe/issues/11)

* Version 1.9
  - added two keys (letter and other) to Code Keys (see manual)
  - setting, by default, _:@ as letters (for expl3) [\#9](https://github.com/alceu-frigeri/codedescribe/issues/9)
  - added a few option keys to further customize \tsobj (bnf style lists, see manual)
  - documentation review (typos, clarity).
  - code cleanup.

* Version 1.8
  - fixes
    [\#6](https://github.com/alceu-frigeri/codedescribe/issues/6), [\#7](https://github.com/alceu-frigeri/codedescribe/issues/7) and
    [\#8](https://github.com/alceu-frigeri/codedescribe/issues/7).
  - Added an (optional) index parameter to the code display/demo commands.
  - New command: \tsmergedcode, \tsexec and \setnewcodekey (see documentation).


* Version 1.7
  - fixing  [\#4](https://github.com/alceu-frigeri/codedescribe/issues/4) (hopefully) for good and 
  - working on [\#5](https://github.com/alceu-frigeri/codedescribe/issues/5). 
  - Added an environment <tsremark*> (see documentation). 

* Version 1.6
  - fixing issue [\#3](https://github.com/alceu-frigeri/codedescribe/issues/3) (long standing (hidden) bug. 
    \tsresult now fully respects optional keys.

* Version 1.5b 
  - fixing issue [\#2](https://github.com/alceu-frigeri/codedescribe/issues/2) (reverting `codesyntax` bug introduced by v1.5). 

* Version 1.5
  - fixing issue [\#1](https://github.com/alceu-frigeri/codedescribe/issues/1) (misalignment when missing a `codesyntax` inner environment). 

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
