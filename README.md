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

    The `<name>` part can be either `*` or `**` instead of a valid logo
    name. There `*` means “all the primary logo names” and `**` means
    “all the secondary logo names”.  (The logo classification will be
    described later.) For example, `{*,my+**}` imports all the primary
    logos (without prefix, non-forcefully) and then imports forcefully all
    the secondary logos with prefix `my`.

    Note that the logo names explicitly given earlier are excluded from
    the bulk import by `*` and `**`. For example, `{BibTeX,my-*}` defines
    `\BibTeX` and `\myXeTeX` but not `\myBibTeX`.

  * `\bxtexlogoImport{<name>,...}`: The same as `\bxtexlogoimport`, except
    that the logo names explicitly given are not excluded from the target
    of bulk imports in the future. This command is intended to be used in
    packages and classes.

  * `\bxtexlogo{<name>}: Outputs the logo of name `<name>`. This form can
    be always used, whether the logo is imported or not.

### Parameter settings

The `\bxtexlogosetup` command can be used to configure the behavior of
the package.

    \bxtexlogosetup{<key>=<value>,...

* Boolean values are specified as `true` or `false`.

The following setting keys are available:

  * `smallcaps=<value>`: Whether or not fake smallcaps is used.
      - `real`: The real smallcaps font face (shape `sc`) is used.
      - `fake`: The fake smallcaps (capital letters in reduced size)
        is used.
      - `auto` (default): The fake smallcaps is used only for the
        following specific font faces:
        CM Sans Serif and LM Sans Serif.
  * `one-font=<value>`: Which font family is used for the letter ‘1’
    in the 1TeX logo.
      - `normal`: The normal setting, where the dsrom family is used
        most preferentially. This setting lacks bold series.
      - `bboldx`: The bboldx family is always used. This family has
        bold series.
  * `hologo-for-basic=<bool>`: This parameter controls how to render
    the `TeX`, `LaTeX` or `LaTeX2e` part of the logos provided by this
    package (such as `XyMTeX`). If true, the definitions provided by the
    hologo package are used; if false, the current definitions of the
    commands `\TeX`, `\LaTeX` and `\LaTeXe` are used.
  * `ghost=<bool>`: Whether or not a 'ghost' is inserted around logos
    in order to improve rendering in the Japanese typesetting.

### Avaiable logo names

The logo names supported by this package are divided into two classes:
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

  * `ApTeX`
  * `CSTUG`
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
  * `OpTeX`
  * `pTeXsT`
  * `XyM` for prefix
  * `XyMTeX`
  * … and more exotic ones, such as `BaSiX`  
    (See the sample document for detail.)

#### Addtional logos

Starting from v0.6, *all* hologo logos (not only ones classified as
“primary” or “secondary”) can be imported through `\bxtexlogoimport`
command, as long as its name contains only letters. For example, the logo
`Xe` (the head part of the `XeTeX` logo) that is provided by hologo can
be imported by invoking `\bxtexlogoimport{Xe}`, and then you can output
this logo by typing `\Xe`. (You can also do `\bxtexlogoimport{my-Xe}`
instead, of course.) Note that these “non-classified” logos are never
included in the target of bulk import.

Note. The command `\bxtexlogo` also supports all hologo logos and thus
can be used in place of `\hologo`, just if you like it.

Moreover, the bxtexlogo itself provides a few “non-classified” logos,
such as `e` (the head part of `eTeX` logo). This logo can be used by
importing (perhaps with a prefix) or by writing `\bxtexlogo{e}`. See the
sample document for detail.

### Notices

  * You are recommended to load the graphicx package; its functionality
    will be utilized to improve the output of logos.
  * You cannot use the logo commands in math mode.
  * You can use the logos provided by this package in PDF strings, but
    not in TeX4ht workflow (contrary to the logos provided by hologo).
  * The functionality of the hologo package is not altered in any way.
  * You cannot apply the management commands of hologo (`\hologoSetup`
    etc.) to the logos provided by this package.


The bxtexlogo-primary Package
-----------------------------

### Package Loading

    \usepackage[<option>,...]{bxtexlogo-primary}

### Usage

This is an alternative entrypoint to the bxtexlogo package. It loads
bxtexlogo and “reserves” the bulk import of all the primary logos
as the default action. If the author never uses `\bxtexlogoimport`,
then the package runs `\bxtexlogoimport{*}` in the begin-document hook.

*Note.* In fact, the bxtexlogo package itself has had the same feature,
despite that the documentation says nothing about it. Starting with
v0.8, this feature is *deprecated* for future removal and a warning will
be issued for the use of implicitly imported commands. You should use
the bxtexlogo-primary package instead if you need the feature.


Revision History
----------------

  * Version 0.8 ‹2026/05/23›
      - More logo: `Prote`.
      - Add `\bxtexlogosetup` for parameter setting.
      - Add parameters: `one-font`, `smallcaps`, `fake-smallcaps-for`,
        `hologo-for-basic`, `ghost`.
      - Better support for dvips and dvisvgm.
      - Support for use in csname strings (as per hologo).
      - Support for “ghost” insertion for Japanese typesetting.
      - Warn the use of implicit imports.
      - Add new package `bxtexlogo-primary`.

  * Version 0.7a ‹2026/05/15›
      - Bug fix.

  * Version 0.7 ‹2026/04/29›
      - More logos: `HiLaTeX`, `LuaMetaTeX`, `lowe`.
      - Bug fix.

  * Version 0.6 ‹2022/05/05›
      - More logos: `HiTeX`, `TeX--XeT`.
      - Add `\bxtexlogo`.
      - Add `\bxtexlogoReflect`.

  * Version 0.5 ‹2021/11/11›
      - More logos: `OpTeX`, `CSTUG`.
      - (experimental) Add `\bxtexlogoUseBboldx`.

  * Version 0.4 ‹2018/03/11›
      - More logos: `ApTeX`, `DVIPDFMx`.
      - Add `\bxtexlogoItalicOrSlant`.

  * Version 0.3 ‹2017/11/11›
      - More logos.

  * Version 0.2a ‹2016/11/11›
      - Bug fix.

  * Version 0.2  ‹2016/04/01›
      - The first public version.

--------------------
Takayuki YATO (aka. "ZR")  
https://github.com/zr-tex8r
