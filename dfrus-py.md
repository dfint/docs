## [< Home](https://bitbucket.org/dfint/dfint-docs/wiki/Home)

# [dfrus-py](https://bitbucket.org/dfint/dfrus-py/src) subproject files:
Language: Python 3
## Executable modules
* **dfrus.py** - a script intended to be replacement of the `dfrus034.exe`/`dfint.exe`. Now it more or less functional, but needs more testing. Usage examples will be added soon.
* **extract_strings.py** - a utility program which extracts hardcoded strings from the Dwarf Fortress.exe. Compatible with Python2.7
    * **Usage:** `python extract_strings.py "Dwarf Fortress.exe" > stringdump.txt`
* **edit_relocs.py** - a program to fix [relocation entries](https://en.wikipedia.org/wiki/Relocation_%28computing%29) of a file of the Portable Executable format.
    * **Usage:**
        * To add specific entries: `python file.exe + 0x123 0x345 0x567`
        * To remove specific entries: `python file.exe - 0x123 0x345 0x567`
        * To remove a range of entries (eg. remove all the relocations of an old version of a procedure): `python file.exe -* 0x123 0x567`

## Importable modules

* **binio.py** - some binary i/o functions;
* **patchdf.py** - some utility functions specific to the DF;
* **pe.py** - module to work with the Portable Executable format;
* **disasm.py** - there will be implemented some basic disassembly engine.