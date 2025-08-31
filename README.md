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
