[![Actions Status](https://github.com/tbrowder/CSV-Tools/actions/workflows/linux.yml/badge.svg)](https://github.com/tbrowder/CSV-Tools/actions) [![Actions Status](https://github.com/tbrowder/CSV-Tools/actions/workflows/macos.yml/badge.svg)](https://github.com/tbrowder/CSV-Tools/actions) [![Actions Status](https://github.com/tbrowder/CSV-Tools/actions/workflows/windows.yml/badge.svg)](https://github.com/tbrowder/CSV-Tools/actions)

NAME
====

**CSV::Tools** - Provides Raku programs and routines to manage CSV tables.

SYNOPSIS
========

```raku
use CSV::Tools;
```

DESCRIPTION
===========

**CSV::Tools** provides the following program:

  * create-csvdb <My.csv> | <My.yml> [...options...]

With a CSV file name entry, the following files are created with names based on the input file name without the '.csv' suffix:

    ./lib/My.rakumod
    $HOME/.raku/bin/manage-my

For customized names, use a YAML configuration file with the following format:

    csv: </path/to/source csv file>
    lib: </path/to/some.rakumod>
    bin: <desired management file name> # this file will be placed
                                        # in the user's $HOME/.raku/bin
                                        # directory

Without options, the program does the following:

+ Uses the CSV file name to create names for

- a management program

- a module in ./lib which is used by the generated program

Options include allowing: customization with a YAML configuration file.

AUTHOR
======

Tom Browder <tbrowder@acm.org>

COPYRIGHT AND LICENSE
=====================

© 2024 Tom Browder

This library is free software; you may redistribute it or modify it under the Artistic License 2.0.

