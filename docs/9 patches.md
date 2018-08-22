# Patches Opatch


##Instalación
 
Al igual que los demás plug-ins, para instalarse ir al menú Plug-ins > Install > WebLogic 11g (o WebLogic 12c) > Patches [OPatch] y seleccionar la ruta del jar del plugin. 
Nota: No es necesario especificar un Oracle Home

*Click Plug-Ins > Install > WebLogic 12c > Patches[OPatch]*

![1 menu patches](/img/patches/1menu-patches.jpg)

En la siguiente pantalla se deberá seleccionar el plug-in a instalar, se solicitará el jar del plugin WebLogic 12cPatches.jar

![2 instalar plugin](/img/patches/2instalar-plugin.jpg)

***Browse*** Este botón permite seleccionar el archivo .zip que contiene los binarios de instalación.


Al finalizar el proceso de instalación será requerido el reinicio de Vesta para la aplicación del plug-in.

![3 msg reinicio](/img/patches/3msg-reinicio.jpg) 

## Configuracion de plug-on Patches[OPatch]

Para obtener las entradas de configuracion relacionadas a parches de OPatch en un ambiente hay que seleccionar la opcion Configure del menú Plug-ins


***Click Plug-Ins > Configure***

![4 menú configure](/img/patches/4menu-configure.jpg)

En la siguiente pantalla se deberá seleccionar la “Aplicación y Ambiente” al cual estará asociado el Plug-in “Patches[OPatch]”. Es importante conocer que una misma “Aplicación y Ambiente” pueden estar asociados a múltiples plug-ins.

![5 sel plugin](/img/patches/5sel-plugin.jpg)

A continuación, será solicitado el archivo .patch para la creación de las entradas de configuración.

![6 archivo patch](/img/patches/6archivo-patch.jpg)

***Browse*** Este botón permite seleccionar un archivo con extensión .patch para realizar el import de entradas de configuración a Vesta.

> Nota: Para generar el archivo .patch debe ir al <ORACLE_HOME>/OPatch  en el server donde corre su instalación de WebLogic y debe correr el siguiente comando.

> ./opatch lsinventory > lsinventory.patch  (para Linux)

> .\opatch lsinventory > lsinventory.patch (para Windows)

> El archivo lsinventory.patch debe descargarse al host donde corre Vesta para abrirlo en este paso de la configuración del plugin Patches[OPatch]


### Listar entradas “Patches [OPatch]”

Una vez seleccionado el archivo .patch serán cargadas las entradas de configuración en Vesta.

Así podemos tener almacenada la configuración de los parches instalados en el Oracle Home de la instalación de WebLogic.

![7 listar entradas](/img/patches/7listar-entradas.jpg)

## Opciones sobre entradas

![8 opc entries](/img/patches/8opc-entries.jpg)


Las siguientes opciones se encuentran descritas en la sección Configuración inicial > [Opciones sobre entradas](/opciones.md)> 

* View entry
* Edit entry
* Duplicate entry
* Promote entry
* Delete entry
* View children
* View History
* Tree History
* Copy Selection
* Copy property
* Compare


