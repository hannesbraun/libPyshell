# Pyshell

A python module for writing shell-scripts in Python. It introduces
new functionality, bundles functions distributed over several modules of
Python's standard library in one place and provides several auxiliary functions.

The function's provided by the `shell` module are named after the corresponding
Unix commands.

Here's a quick demo:

~~~python
from shell import *

rm('a/b/foo.txt')
mv('X.pdf', f'{HOME}/contents.pdf')

files = ls('Documents', '*.txt', '*.c')
magicFiles = run(['grep', 'magic'] + files, captureStdout=splitLines, onError='ignore').stdout
~~~

* Requirements: Python 3
* [API documentation](https://htmlpreview.github.io/?https://github.com/skogsbaer/libPyshell/blob/main/doc/shell.html)
* [PyPI page](https://pypi.org/project/libPyshell/)
* Installation: `pip install libPyshell`

## Changelog

* 0.1.5 and 0.1.6 (2023-03-03)
  * Some bugfixes

* 0.1.4 (2022-03-17)
  * Flush stdout and stderr before running a command
