# PdbGen

## Overview

A small utility to generate a dummy PDB with the specified list of public symbols.
This can be used to manually name functions if a PDB file is unavailable.

To generate the PDB file `foo.pdb` for an existing module `foo.dll` run:

    PdbGen foo.dll foo-symbols.txt foo.pdb

`foo-symbols.txt` is a simple text file with each line containing a symbol name
and its RVA in the module (separated by a tab character):

    ?Foo@@YAXXZ	1968328
    Bar	1968328

## Building

Requires [LLVM](https://llvm.org/) libraries to build. Rename `LLVMPDB.props.example`
to `LLVMPDB.props` and change the paths to the LLVM source and build directories.

## License

Code licensed under the [MIT License](LICENSE.txt).
