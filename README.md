# PHyB: Python Hypertext Builder

PHyB (/fɪb/) is a simple (cursed) hypertext builder/processor using python in
less than 200 lines of code.

## Requirements

You need python 3.6+ for PHyB to work.

## Usage

To run PHyB on a single file use:

```sh
./phyb ./website/index.phb ./build/index.html
```

To run PHyB on a folder use:

```sh
./phyb ./website/ ./build/
```

The usage string currently looks like this:

```text
usage: phyb [-h] [-v] INPUT_PATH [OUTPUT_PATH]

PHyB: Python Hypertext Builder.

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

## Extra

PHyB is currently used to generate my website [polyomino.xyz](https://polyomino.xyz/index.html).
