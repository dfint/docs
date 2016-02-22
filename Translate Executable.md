# How to apply translation from transifex to the Dwarf Fortress.exe

## Python 3 installation

* Download and install Python 3 from the official website: https://www.python.org/downloads/windows/
* Python 3.4.4 version is preferred, so download and execute `Windows x86 MSI installer` or `Windows x86-64 MSI installer` depending on which Windows version you have. If you are not sure about Windows version, just download and execute `Windows x86 MSI installer`.

## Downloading translation of the hardcoded strings from the transifex

* Go to the translation project page: https://www.transifex.com/dwarf-fortress-translation/dwarf-fortress/
* Choose your language. Click on it.
* Click on `DF.exe hardcoded strings` resource
* Click on the `Download file to translate` link in the window, which will be shown after the previous action.
* Translation file with `.po` extension will be downloaded.

## Conversion `.po` into `.csv` intermediate format with the appropriate encoding

* Download 