## Beamer theme for the New Economic School

`beamerthemenes` is a package which adds the [New Economic School](https://www.nes.ru) colors
and logo to the nice clean [Metropolis Beamer theme](https://github.com/matze/mtheme).

## System requirements

* Sufficiently new TeXLive or MikTeX distribution (TeXLive 2019 works).
* LuaTeX (`luatex` package in TeXLive)
* Fira Sans and Fira Mono fonts (`fira` package in TeXLive)
* Fira Math font (`firamath-otf` package in TeXLive)
* Metropolis theme (`beamertheme-metropolis` package in TeXLive)
* [NES logo package](https://github.com/sgolovan/neslogo)

## Installation

Just put all the `.sty` files into your TEXMF tree,
typically either into `%USERPROFILE%/texmf/tex/latex/beamer/nes/` (on MS Windows),
or into `$HOME/texmf/tex/latex/beamer/nes/` on Linux.

## Usage

As usual, put into your document's preamble

```
\documentclass{beamer}
\usetheme{nes}
```

and build your presentation using LuaLaTeX. You'll see a NES logo at the
titlepage and a smaller one in the frame titles. Also, the NES blue/red color
scheme will be applied to the slides.

Since `nes` is a thin wrapper around `metropolis`, it inherits all the options
which can be found in the
[Metropolis manual](http://mirrors.ctan.org/macros/latex/contrib/beamer-contrib/themes/metropolis/doc/metropolistheme.pdf).
Additional options are:

#### `logo language`

(`auto`, `russian`, or `english`) Chooses the NES logo language. `auto` means that the language
is taken from `babel` or `polyglossia` settings.

#### `titleformat font family`

(`auto`, `fira`, or `humanist`) Chooses the font for the main title and for frame titles.
`auto` means that if the *Humanist531 BT* font is installed (it's a commercially available
font which is used in NES logos) then it is used in the titles, otherwise *Fira Sans*
substitutes it.

The `nes` theme also changes default settings for a few Metropolis options:

* `numbering` is now equal to `fraction` by default
* blocks are now filled (by light-grey color) by default

## Examples

TODO

## License

The theme itself is licensed under a [Creative Commons Attribution-ShareAlike
4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/). This
means that if you change the theme and re-distribute it, you *must* retain the
copyright notice header and license it under the same CC-BY-SA license. This
does not affect the presentation that you create with the theme.
