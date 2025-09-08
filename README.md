Personal CV using LaTeX. English and Hybrid (Chinglish) versions.

Feel free to use the template as you wish :)

### Docker image

Build using the repo's `Dockerfile`:
```
$ docker build -t cv .
```

Alternatively, use the pre-built packaged image:
```
$ docker pull ghcr.io/gsalinaslopez/cv:release
```

Run xelatex inside the container
```
$ docker run -it -v $(pwd):/workdir --rm cv bash
# pwsh
# docker run -it -v "${PWD}:/workdir" --rm cv bash

root@container-id:/workdir# xelatex ...
```

Conver pdf to png using [ImageMagick](https://imagemagick.org/)
```
// add [#pp] for multipage pdf: i.e. file.pdf[2] for 3rd page
convert -flatten -density 300 file.pdf -quality 90 file.png
```

### Fonts

[Source Serif Pro](https://fonts.google.com/specimen/Source+Serif+Pro#license) for the title and headings.

[Source Sans Pro](https://fonts.google.com/specimen/Source+Sans+Pro#license) for content description.

[Source Han Serif](https://github.com/adobe-fonts/source-han-serif) for the Chinese characters.

### Credit

This scaffold is forked from https://github.com/gsalinaslopez/cv, thanks to [Giovanni Salinas](https://github.com/gsalinaslopez)

Template for cover letter taken from: https://tex.stackexchange.com/questions/583798/newlfm-expect-new-fancyhdr-sty-but-its-the-newest, thanks to [Werner](https://tex.stackexchange.com/users/5764/werner)
