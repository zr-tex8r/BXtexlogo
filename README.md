BXtexlogo Package
=================

LaTeX: Additional TeX-family logos

Blah....

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

```tex
\usepackage[<option>,...]{bxtexlogo}
```

All the options are passed to hologo.

### Usage

You can import logo commands with `\bxtexlogoimport` in your document's preamble.

```tex
\bxtexlogoimport{<name>,...}
```

You can also specify `*` for importing all commands in level 1, and `**` for level 2. Here is an example to import every level 1 commands and `\OneTeX` command.

```tex
\bxtexlogoimport{*,OneTeX}
```

#### List of logo commands

| Level | Name          | Command          |
| --:   | :--           | :--              |
| 1     | pTeX          | `\pTeX`          |
| 1     | epTeX         | `\epTeX`         |
| 1     | pLaTeX        | `\pLaTeX`        |
| 1     | pLaTeXe       | `\pLaTeXe`       |
| 1     | upTeX         | `\upTeX`         |
| 1     | eupTeX        | `\eupTeX`        |
| 1     | upLaTeX       | `\upLaTeX`       |
| 1     | upLaTeXe      | `\upLaTeXe`      |
| 1     | JBibTeX       | `\JBibTeX`       |
| 1     | pBibTeX       | `\pBibTeX`       |
| 2     | JTeX          | `\JTeX`          |
| 2     | JLaTeX        | `\JLaTeX`        |
| 2     | pTeXsT        | `\pTeXsT`        |
| 2     | XyMTeX        | `\XyMTeX`        |
| 2     | KETpic        | `\KETpic`        |
| 2     | logoOmega     | `\logoOmega`     |
| 2     | logoLambda    | `\logoLambda`    |
| 2     | logoAleph     | `\logoAleph`     |
| 2     | logoLamed     | `\logoLamed`     |
| 2     | BaSiX         | `\BaSiX`         |
| 2     | TeXonLaTeX    | `\TeXonLaTeX`    |
| 2     | OneTeX        | `\OneTeX`        |
| 2     | SuyahTeX      | `\SuyahTeX`      |
| 2     | YukidarumaTeX | `\YukidarumaTeX` |

Revision History
----------------

  * Version 0.2a ‹2016/11/11›
      - Bug fix.

  * Version 0.2  ‹2016/04/01›
      - The first public version.

--------------------
Takayuki YATO (aka. "ZR")  
http://zrbabbler.sp.land.to/
