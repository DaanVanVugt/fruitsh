# Fruit.sh, a simple bash driver for Fortran Unit Testing
The [`FORTRAN` Unit Test Framework (`FRUIT`)](https://sourceforge.net/projects/fortranxunit/) is a neat system for unit testing.
To simplify its usage a driver program comes in handy, like the one in this repository.
It's written in bash, and has very few dependencies (`find`, `grep` and `sed`).
You can specify individual files and directories to test, and even run individual tests.

`XML` and `junit` output are supported.

## Installation
Place `fruit.sh` into your `PATH` and make it executable.

## Usage
```
Usage: fruit.sh [-hk] [-t <type> --type=<type>] <file/dir>...

  <file/dir> A file or directory containing FRUIT test (files).
  -h         Print this usage information and exit
  -k         Keep the generated test executable and source file (for running in GDB)
  -t <type>  Type of output. Either none, junit or xml (default none)
  -s <name>  Test only a single subroutine if specified
"
The executable created will have a temporary file name.
```
For example
```bash
fruit.sh tests/file1.f90 tests/dir2
```
or
```bash
fruit.sh tests/file1.f90 -s test_only_this_routine
```

## Contributing
Pull requests are welcome!

## License
MIT, see license.txt
