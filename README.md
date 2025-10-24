# Photo Tools

A collection of photography-related command line utilities.

### Border

```text
Adds a border to an image, and, optionally, converts the image to a different
aspect ratio.

Usage: border [OPTIONS] FILE

Options:
  -c COLOR
        Set color of the border.
        Default: white.
  -w WIDTH
        Set minimal width of the border, as a percentage of the original
        height (if the new aspect ratio is wider than the original one)
        or the original width (if the new aspect ratio is taller than the
        original one).
        Default: 2.
  -r RATIO
        Aspect ratio of the new image in the format wxh, for example: 2x3.
        Default: unchanged.
```

### Collage

```text
Combines two images into a collage, separated and surrounded by a border.

Usage: collage [OPTIONS] FILE1 FILE2

Options:
  -h
        Make a horizontal collage.
  -v
        Make a vertical collage.

        If -h and -v are not set, portrait images will result in a horizontal
        collage, and landscape images in a vertical one.

  -c COLOR
        Set color of the border.
        Default: white.
  -w WIDTH
        Set minimal width of the outer border, as a percentage of the original
        height (in case of a horizontal collage) or the original width (in case
        of a vertical one).
        Default: 2.
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
