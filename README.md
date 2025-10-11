# Photo Tools

A collection of photography-related command line utilities.

### Border

```
Adds a border to an image, and, optionally, converts the image to a different aspect ratio.

Usage: border [-c color] [-w width] [-r wxh] file

Options:
  -c color
        Color of the border.
        Optional, default: white.
  -w width
        Minimal width of the border, as a percentage of the original height (if the new aspect ratio is wider
        than the original one) or the original width (if the new aspect ratio is taller than the original one).
        Optional, default: 2.
  -r wxh
        Aspect ratio of the new image in the format wxh, for example: 2x3.
        Optional, default: unchanged.
```

### Collage

```
Combines two images into a collage, separated and surrounded by a border. Portrait images will result in a landscape
(horizontal) collage, and landscape images result in a portrait (vertical) collage.

Usage: ../bin/collage [-c color] [-w width] [-r wxh] file

Options:
  -c color
        Color of the border.
        Optional, default: white.
  -w width
        Minimal width of the outer border, as a percentage of the original height (in case of a landscape collage)
        or the original width (in case of a portrait one).
        Optional, default: 2.
```

## Installation

The scripts should be placed in a directory that is on your `$PATH`, and they should be executable. For example:

```shell
git clone https://github.com/hielke84/photo-tools.git
cd photo-tools
chmod +x bin/*
cp bin/* ~/bin
```

Then add the following to your `~/.bashrc`:

```shell
export PATH="$HOME/bin:$PATH";
```

and restart your terminal.
