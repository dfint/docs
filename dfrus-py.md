[< home](https://bitbucket.org/dfint/dfint-docs/wiki/Home)

# [dfrus-py](https://bitbucket.org/dfint/dfrus-py/src) subproject files:

## Executable modules
* `dfrus.py` - a script intended to be replacement of the `dfrus034.exe`/`dfint.exe`. Implemented about 20-30% of the planned functionality.
* `extract_strings.py` - a utility program which extracts hardcoded strings from the Dwarf Fortress.exe.
    * **Usage:** `python extract_strings.py "Dwarf Fortress.exe" > stringdump.txt`
* `edit_relocs.py` - a program to fix relocation entries of a portable executable.
    * **Usage:**
        * To add specific entries: `python file.exe + 0x123 0x345 0x567`
        * To remove specific entries: `python file.exe - 0x123 0x345 0x567`
        * To remove a range of entries: `python file.exe -* 0x123 0x567`

## Importable modules

* `binio.py` - some binary i/o functions;
* `patchdf.py` - some utility functions specific to the DF;
* `pe.py` - module to work with the Portable Executable format;
* `disasm.py` - there will be implemented some basic disassembly engine.