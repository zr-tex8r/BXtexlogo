BXtexlogo Package
=================

LaTeX: Additional TeX-family logos

The package [hologo] enables you to output many useful logos of popular
(and not so popular) TeX-family software. However its interface is a bit
cumbersome because you must type `\hologo{BibTeX}` instead of `\BibTeX`.
This package enables you to import some of logos provided by hologo as
simgle commands, such as `\BibTeX`.

Moreover this package provides yet additional logos of TeX-family software
most of which is popular mainly in Japan. These logos can be imported in
the same way as those provided by hologo.

[hologo]: https://ctan.org/pkg/hologo

### System requirement

  * TeX format: LaTeX.
  * TeX engine: Anything.
  * Dependent packages:
      - hologo
      - cjhebrew (if `\logoAleph` and `\logoLamed` are used)

### Installation

  - `*.sty` → $TEXMF/tex/latex/BXtexlogo

### License

This package is distributed under the MIT License.


The bxtexlogo Package
---------------------

### Package Loading

    \usepackage[<option>,...]{bxtexlogo}

All the options are passed to hologo.

### Usage

  * `\bxtexlogoimport{<name>,...}`: Defines a command to output the logo
    specified by `<name>`. For example, `\bxtexlogoimport{BibTeX}` defines
    the command `\BibTeX` to output the `BibTeX` logo, if the command is
    undefined. Alternatively, a list element in the argument can have
    the following forms:
      - `+<name>`: Defines forcefully; for example, `+BibTeX` defines the
        command `\BibTeX` even if the command is already defined.
      - `<prefix>-<name>`: Defines with a prefix; for example, `my-BibTeX`
        defines the command `\myBibTeX` for the logo `BibTeX`, if the
        command is undefined.
      - `<prefix>+<name>`: Defines forcefully with a prefix; for example,
        `my+BibTeX` overwrites the command `\myBibTeX`.

    The `<name` part can be either `*` or `**` instead of a valid logo
    name. There `*` means “all the primary logo names” and `**` means
    “all the secondary logo names”.  (The logo classification will be
    described later.) For example, `{*,my+**}` imports all the primary
    logos (without prefix, non-forcefully) and then imports forcefully all
    the secondary logos with a prefix.

    Note that the logo names explicitly given earlier are excluded from
    the bulk import by `*` and `**`. For example, `{BibTeX,my-*}` defines
    `\BibTeX` and `\myXeTeX` but not `\myBibTeX`.

  * `\bxtexlogoImport{<name>,...}`: The same as `\bxtexlogoimport`, except
    that the logo names explicitly given are not excluded from the target
    of bulk imports in the future. This command is intended to be used in
    packages and classes.

### Avaiable logo names

The logo names supported by this package are divides into two classes:
“primary” (popular software) and “secondary” (all others).

#### Primary logos

You can bulk-import the primary logos with `\bxtexlogoimport{*}`.

(Logos provided by hologo)

  * `AmSLaTeX`
  * `AmSTeX`
  * `BibTeX`
  * `ConTeXt`
  * `eTeX`
  * `LaTeX`
  * `LaTeXe` for “LaTeX 2ε” logo
  * `LuaLaTeX`
  * `LuaTeX`
  * `LyX`
  * `METAFONT`
  * `METAPOST`
  * `pdfTeX`
  * `pdfLaTeX`
  * `TeX`
  * `XeLaTeX`
  * `XeTeX`

(Logos provided by this package)

  * `epTeX` for “ε-pTeX” logo
  * `eupTeX` for “ε-upTeX” logo
  * `JBibTeX` (old version of pBibTeX)
  * `pBibTeX`
  * `pLaTeXe` for “pLaTeX 2ε”
  * `pLaTeX`
  * `pTeX`
  * `TikZ`
  * `upBibTeX`
  * `upLaTeX`
  * `upLaTeXe` for “upLaTeX 2ε”
  * `upTeX`

#### Secondary logos

You can bulk-import the secondary logos with `\bxtexlogoimport{**}`.

(Logos provided by hologo)

  * `HanTheThanh` for “Hàn Thế Thành”
  * `KOMAScript`
  * `LaTeXTeX` for “(La)TeX”
  * `NTS`
  * `PiCTeX`
  * `SageTeX`
  * `SLiTeX`
  * `teTeX`
  * `TTH`

(Logos provided by this package)

  * `HeVeA`
  * `JBibTeX`
  * `JLaTeX`
  * `JTeX`
  * `KaTeX`
  * `KET` for prefix
  * `KETpic`
  * `LaTeXiT`
  * `LaTeXML`
  * `logoAleph` for “א”
  * `logoLambda` for “Λ”
  * `logoLamed` for “ל”
  * `logoOmega` for “Ω”
  * `pTeXsT`
  * `XyM` for prefix
  * `XyMTeX`
  * … and more exotic ones, such as `BaSiX`  
    (See the sample document for detail.)

### Notices

  * You are recommended to load the graphicx package; its functionality
    will be utilized to improve the output of logos.
  * You cannot use the logo commands in math mode.
  * You can use the logos provided by this package can be used in PDF
    strings, but not in TeX4ht workflow (contrary to the logos provided by
    hologo).
  * The functionality of the hologo package is not altered in any way.
  * You cannot apply the management commands of hologo (`\hologoSetup`
    etc.) to the logos provided by this package.


Revision History
----------------

  * Version 0.3 ‹2017/11/11›
      - More logos.

  * Version 0.2a ‹2016/11/11›
      - Bug fix.

  * Version 0.2  ‹2016/04/01›
      - The first public version.

--------------------
Takayuki YATO (aka. "ZR")  
http://zrbabbler.sp.land.to/
