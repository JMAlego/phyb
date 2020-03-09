# FobIt

Simple (cursed) static website generation with python in less than 200 lines of code.

## Requirements

You need python 3.6+ for fobit to work.

## Usage

To run fobit on a single file use:

```
./fobit ./website/index.fob ./build/index.html
```

To run fobit on a folder use:

```
./fobit ./website/ ./build/
```

The usage string currently looks like this:

```
usage: fobit [-h] [-v] INPUT_PATH [OUTPUT_PATH]

fobit fobs off static website generation (mostly) to python.

positional arguments:
  INPUT_PATH
  OUTPUT_PATH

optional arguments:
  -h, --help     show this help message and exit
  -v, --version  show program's version number and exit
```

## Examples

Here's an example simple page:

```html
{!
from datetime import date
!}
<!doctype html>
<html>

  <head>
    <title>Simple little page.</title>
  </head>

  <body>
    <p>This page was generated on {$ date.today() $}.</p>
  </body>

</html>
```

Which would produce the following output (well if the date was 2020-03-09):

```html
<!doctype html>
<html>

  <head>
    <title>Simple little page.</title>
  </head>

  <body>
    <p>This page was generated on 2020-03-09.</p>
  </body>

</html>
```