# Dwarf Fortress i18n Project

## Project parts:

* [dfrus patch](https://bitbucket.org/insolor/dfrus/) for hardcoded strings. Language: OpenEuphoria 4.0.5
    * [Its latin-only version](https://bitbucket.org/dfint/df-i18n) (somewhat outdated). Language: OpenEuphoria 4.0.5
    * [dfrus-py](https://bitbucket.org/dfint/dfrus-py) - an attempt to translate dfrus from Euphoria to Python + some usefull toolkit. Language: Python 3.4
* Changetext project group:
    * [Fake_ttf.dll](https://bitbucket.org/dfint/fake_ttf.dll) - source code of proxy dll, which intercepts text passed from Dwarf Fortress.exe to SDL_ttf.dll and redirects it to changetext.dll. Language: Assembly (fasm)
    * [changetext.dll](https://bitbucket.org/dfint/changetextpy) - utility library which changes a text passed to it from Fake_ttf.dll using external script in Python - changetext.py. Language: C.
    * [changetext.py](https://bitbucket.org/dfint/changetextpy_script) - the script which refines Russian tranlsation (word order, inclination, etc.). Language: Python 3.4.
* ***TODO:*** add description for [dfgettext](https://bitbucket.org/dfint/df-gettext-toolkit), [stringdumps](https://bitbucket.org/dfint/stringdumps), [df-manager](https://bitbucket.org/dfint/df-manager), [addcoloredst-temp](https://bitbucket.org/dfint/addcoloredst-temp)