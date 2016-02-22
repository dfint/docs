# Dwarf Fortress i18n Project Documentation

## Project parts:

* **[dfrus patch](https://bitbucket.org/insolor/dfrus/)** for hardcoded strings. Language: OpenEuphoria 4.0.5
    * **[dfint.exe](https://bitbucket.org/dfint/df-i18n)** - its latin-only version (somewhat outdated). Language: OpenEuphoria 4.0.5
    * **[dfrus-py](https://bitbucket.org/dfint/dfrus-py)** - an attempt to translate dfrus from Euphoria to Python + some usefull toolkit. [**Some documentation**](dfrus-py). Language: Python 3.4.
    * **[stringdumps](https://bitbucket.org/dfint/stringdumps)** - lists of hardcoded strings of DF versions from 0.34.10 through *[the most recent DF version number]* used as templates for translation.
* Changetext project group:
    * **[Fake_ttf.dll](https://bitbucket.org/dfint/fake_ttf.dll)** - proxy dll, which intercepts text passed from Dwarf Fortress.exe to SDL_ttf.dll and redirects it to changetext.dll. Language: Assembly (fasm)
    * **[changetext.dll](https://bitbucket.org/dfint/changetextpy)** - utility library which changes a text passed to it from Fake_ttf.dll using external script in Python - changetext.py. Language: C.
    * **[changetext.py](https://bitbucket.org/dfint/changetextpy_script)** - the script which refines Russian tranlsation (word order, inclination, etc.). Language: Python 3.4.
* Manual patches:
    * **[df-manager](https://bitbucket.org/dfint/df-manager)** - rewritten in Assembly and changed version of `standardstringentry()` function, other patches related to search in the DF manager.
    * **[addcoloredst-temp](https://bitbucket.org/dfint/addcoloredst-temp)** - rewritten in Assembly version of `addcoloredst()` function - changed to use `addst()` function instead of using `addchar()` (in order to output text on "Thoughts and Prefences" and similar screens with ttf font).
* **[dfgettext](https://bitbucket.org/dfint/df-gettext-toolkit)** - a set of tools which are used to convert parts of files being translated to the [GNU gettext](http://www.gnu.org/software/gettext/) format and aback. Helps make translation with the specialized tools both offline (like [poedit](http://poedit.net/)) and online (like [transifex.com](http://transifex.com/)).
* **[www.transifex.com/dwarf-fortress-translation/dwarf-fortress/](https://www.transifex.com/dwarf-fortress-translation/dwarf-fortress/)** - a place where we perform translation.

## Instructions for translators
* [**How to apply translation from transifex to exe-file**](Translate Executable)
* How to apply translation from transifex to the text files
    * How to unpack packed text files (help, some in-game messages, etc.)

***TODO:*** add separate documentation pages for dfgettext, manual patching.