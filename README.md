# PathlibIO

CLI functionality of Python's Pathlib module

A single script `pathlibio` contains the functionality, a wrapper around most of `pathlib.Path`'s methods and properties

Help is available at `pathlibio -h`

Reads from stdin if `-` is passed as the path, performing actions on each line read as a path. In this case test-like functions such as `is_socket` cause the script to exit after the first false result.

## Installation

`$ pip install PathlibIO` from PyPI

## Examples

```
$ pathlibio suffix README.md
.md
$ pathlibio exists README.md && echo Hello
Hello
$ pathlibio is_char_device /dev/tty && echo "It's tty time"
It's tty time
$ echo pyproject.toml | pathlibio with_suffix - .json # in an ideal world...
pyproject.json
```
