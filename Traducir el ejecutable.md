## [<< Home](Home)
# Como aplicar la traducción de transifex al dwarf fortress.exe

## Instalación de Python 3:

* Descargue e instale Python 3 desde la página oficial: https://www.python.org/downloads/windows/
* Es preferible la versión Python 3.4.4, descargue y ejecute `Windows x86 MSI installer` o `Windows x86-64 MSI installer` dependiendo de que versión de Window posea. Si no está seguro de cuál es su versión de Window, descargue y ejecute `Windows x86 MSI installer`.

## Descargar de la traducción de las cadenas encriptadas desde Transifex

* Vaya a la página del proyecto de traducción: https://www.transifex.com/dwarf-fortress-translation/dwarf-fortress/language/es/
* Haga click en el recurso `DF.exe hardcoded strings`.
* Aparecerá una ventana, haga click en el link `Download file to translate` (“Descargar archivo para traducir”).
* Se descargará un archivo de traducción con la extensión `.po`.

## Conversión de `.po` al formato intermedio `.csv` con la codificación adecuada

* Descargue el repositorio completo [df-gettext-toolkit](https://bitbucket.org/dfint/df-gettext-toolkit/) ([**zip**](https://bitbucket.org/dfint/df-gettext-toolkit/get/default.zip)) y descomprímalo en un carpeta separada.
* Coloque allí el archivo `.po`, que descargó anteriormente.
* En la carpeta donde usted descomprimio el archivo zip `df-gettext-toolkit` ejecute el siguiente comando desde una línea de comando:
  
```
python po2csv.py po-filename.po dictionary.csv cp850
```
  
Notas:

* `po-filename.po` debe ser reemplazado por el nombre actual del archivo `.po` descargado
* `cp850` debe ser reemplazado con el DOS-codepage que su lenguaje soporte (puede consultarlo con [esta](http://www.kostis.net/charsets/trans130/cpdos.htm) pagina). Actualmente los codepage soportados son: `cp737` (Griego), `cp850` (Multilenguaje - Latin 1), `cp860` (Portugal), `cp866` (DOS Cirillico), `cp1251` (Cirillico de Window). Si el codepage de su lenguaje no es soportado, puede enviarme un mensaje con su solicitud (ver contactos al final).
* Puede crear un archivo `.bat` con este comando para ejecutarlo con un doble click.

## Aplicar la traducción al ejecutable de Dwarf Fortress

* Como en la sección previa, descargue el repositorio completo [dfrus-py](https://bitbucket.org/dfint/dfrus-py/) ([**zip**](https://bitbucket.org/dfint/dfrus-py/get/default.zip)) y descomprímalo en un carpeta separada.
* Coloque el archivo `dictionary.csv` que usted obtuvo en el paso anterior en esta carpeta.
* Ejecute el siguiente comando desde una línea de comando:

```
python dfrus.py -p "d:\Games\df_42_06_win_s\Dwarf Fortress.exe" -d dictionary.csv --codepage cp850
```

Notas:

* `"d:\...\Dwarf Fortress.exe"` debe ser reemplazado con la ubicación del ejecutable de Dwarf Fortress. El nuevo ejecutable (traducido) será creado en la misma carpeta con el nombre `Dwarf Fortress Patched.exe`.
* `cp850` debe ser reemplazado por el codepage adecuado. Vea sección previa.

## Ultimas preparaciones y ejecución del juego

* Edite init.txt en la carpeta del juego 'data\init', y allí modifique `[TRUETYPE:YES]` y `[PRINT_MODE:2D]`.
* Finalmente, ejecute el `Dwarf Fortress Patched.exe`

## Contacto

Si usted tiene problemas con algunos de los pasos, puede escribirnos un mensaje, intentaremos ayudarlo:

* Aqui, en bitbucket: 
    * [**insolor**](https://bitbucket.org/account/notifications/send/?receiver=insolor) (solo ingles)
    * [**HessedElohim**](https://bitbucket.org/account/notifications/send/?receiver=HessedElohim)
* Mensaje en el foro de “bay12”: 
    * [**insolor**](http://www.bay12forums.com/smf/index.php?action=pm;sa=send;u=72717) (solo ingles)
    * [**Hessed.Elohim**](http://www.bay12forums.com/smf/index.php?action=emailuser;sa=email;uid=114853)
* Mensaje en Transifex.com:
    * [**insolor**](https://www.transifex.com/user/messages/compose/insolor/) (solo ingles)
    * [**Hessed.Elohim**](https://www.transifex.com/user/messages/compose/Hessed.Elohim/)