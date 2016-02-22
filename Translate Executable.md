## [<< Home](Home)
# How to apply translation from transifex to the Dwarf Fortress.exe

## Python 3 installation

* Download and install Python 3 from the official website: https://www.python.org/downloads/windows/
* Python 3.4.4 version is preferred, so download and execute `Windows x86 MSI installer` or `Windows x86-64 MSI installer` depending on which Windows version you have. If you are not sure about your Windows version, just download and execute `Windows x86 MSI installer`.

## Downloading translation of the hardcoded strings from the transifex

* Go to the translation project page: https://www.transifex.com/dwarf-fortress-translation/dwarf-fortress/
* Choose your language. Click on it.
* Click on `DF.exe hardcoded strings` resource
* Click on the `Download file to translate` link in the window, which will be shown after the previous action.
* Translation file with `.po` extension will be downloaded.

## Conversion `.po` into `.csv` intermediate format with the appropriate encoding

* Download the whole [df-gettext-toolkit](https://bitbucket.org/dfint/df-gettext-toolkit/) ([**zip**](https://bitbucket.org/dfint/df-gettext-toolkit/get/default.zip)) repository and unpack it into separate directory.
* Place there the `.po` file, which you've downloaded in the previous section.
* Run the following command from a command line:
  
```
python po2csv.py po-filename.po dictionary.csv cp850
```
  
Notes:
* `po-filename.po` must be replaced with the actual file name of the downloaded `.po` file
* `cp850` must be replaced with the dos-codepage which supports your language (you can consult with [this](http://www.kostis.net/charsets/trans130/cpdos.htm) page). Currently supported codepages are: `cp737` (Greek), `cp850` (Multilingual - Latin 1), `cp860` (Portugal), `cp866` (DOS Cyrillic), `cp1251` (Windows Cyrillic). If codepage of your language is not supported you can send me a message with your request (see contacts in the bottom of this page).
* You can create `.bat` file with this command to run it with a double click.

## Apply translation to the Dwarf Fortress executable

* Like in the previous section, download the whole [dfrus-py](https://bitbucket.org/dfint/dfrus-py/) ([**zip**](https://bitbucket.org/dfint/dfrus-py/get/default.zip)) repository and unpack it into separate directory.
* Place `dictionary.csv` file you've got in the previous section into that directory
* Run the following command from a command line:

```
python dfrus.py -p "d:\Games\df_42_06_win_s\Dwarf Fortress.exe" -d dictionary.csv --codepage cp850
```

Notes:
* `"d:\...\Dwarf Fortress.exe"` must be replaced with the actual path to the Dwarf Fortress executable. The new (translated) executable will be created in the same directory as `Dwarf Fortress Patched.exe`.
* `cp850` must be replaced with the appropriate codepage. See the previous section.

## The last preparations and running the game

* Edit init.txt in the `data\init` directory of the game, and make `[TRUETYPE:YES]` and `[PRINT_MODE:2D]` there.
* Finally, run the `Dwarf Fortress Patched.exe`

## Contacts

If you have troubles with some step here, you can write me a message, I will try to help you:

* Here, on bitbucket: [**insolor**](https://bitbucket.org/account/notifications/send/?receiver=insolor)
* In personal message on bay12forums: [**insolor**](http://www.bay12forums.com/smf/index.php?action=pm;sa=send;u=72717)
* Send a message on transifex.com: [**insolor**](https://www.transifex.com/user/messages/compose/insolor/)
