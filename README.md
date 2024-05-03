## Beamer theme for the New Economic School

`beamerthemenes` is a package which adds the [New Economic School](https://www.nes.ru) colors
and logo to the nice clean [Metropolis Beamer theme](https://github.com/matze/mtheme).

## Prerequisites

* Sufficiently new TeXLive or MikTeX distribution (TeXLive 2023 works).
* LuaTeX (`luatex` package in TeXLive)
* Lato font (`lato` package in TeXLive)
* Fira Mono font (`fira` package in TeXLive)
* Lato Math font (`lato-math` package in TeXLive)
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

#### `logo`

(`true` or `false`) Chooses if the NES logo should be used in slides at all.

#### `logo language`

(`auto`, `russian`, or `english`) Chooses the NES logo language. `auto` means that the language
is taken from `babel` settings (`polyglossia` settings are ignored at the moment).

#### `font family`

(`lato`, `segoe`, or `museo`) Chooses the font for the slides contents.
`lato` chooses the *Lato* font, `segoe` chooses the *Segoe UI* font (it's available in MS Windows distributions),
`museo` chooses the *Museo Sans Cyrl* font, which is a commercial font from the NES brandbook.

#### `titleformat font family`

(`auto`, `lato`, `segoe`, or `museo`) Chooses the font for the main title and for frame titles.
`auto` means the same font as for the contents of the slides, the other values mean the same
as the respective values for the `font family` option.

The `nes` theme also changes default settings for a few Metropolis options:

* `numbering` is now equal to `fraction` by default
* blocks are now filled (by light-grey color) by default

## Examples

Simple [demo slides](https://raw.githubusercontent.com/sgolovan/beamerthemenes/main/demo/demo.pdf).

Default colors, suitable for formal presentations:

![Default colors](https://raw.githubusercontent.com/sgolovan/beamerthemenes/main/examples/colorwhite.png)

The other three color schemes are less formal.

Grey background (`\usecolortheme{nesgrey}`)

![Grey background](https://raw.githubusercontent.com/sgolovan/beamerthemenes/main/examples/colorgrey.png)

Blue background (`\usecolortheme{nesblue}`)

![Blue background](https://raw.githubusercontent.com/sgolovan/beamerthemenes/main/examples/colorblue.png)

Red background (`\usecolortheme{nesred}`)

![Red background](https://raw.githubusercontent.com/sgolovan/beamerthemenes/main/examples/colorred.png)

## License

The theme itself is licensed under a [Creative Commons Attribution-ShareAlike
4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/). This
means that if you change the theme and re-distribute it, you *must* retain the
copyright notice header and license it under the same CC-BY-SA license. This
does not affect the presentation that you create with the theme.
