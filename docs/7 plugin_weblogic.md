# Plug-Ins
---

Los plugins son componentes adicionales de Vesta que le permiten acceder a un aplicativo y descubrir u obtener automáticamente sus configuraciones.

**VESTA** cuenta con una serie de Plug-ins Oracle WebLogic 11g, y WebLogic 12c que permiten la generación automatizada de componentes, estos “Plug-ins” a su vez están encargados de recuperar las configuraciones de los servidores y almacenarlos en la aplicación en modo de “Entradas”, mismas que son asociadas a una aplicación y a un ambiente en particular.

También se dispone de los Plug-ins Oracle SOA Suite 11g y 12g que permiten la administración de configuraciones de componentes principales.

Es importante mencionar que se debe instalar el plugin de acuerdo con la versión de Weblogic que se tenga instalado, por ejemplo, si se cuenta con WebLogic 11g se debe de instalar su plugin de WebLogic 11g.

## Intall WebLogic 11g
---


Se procede a la instalación de WebLogic 11g

*Click  Plug-Ins > Install> WebLogic 11g > General.*

![1 menú plugin](/img/weblogic/1menu-plugin.jpg)

> Nota: El release 11g de WebLogic corresponden a las versiones 10.3.x de WebLogic.


En la siguiente pantalla se deberá seleccionar el plug-in a instalar, se solicitará una serie de archivos y directorios requeridos. Para el caso de los plug-ins de WebLogic 11g y WebLogic 12c, los siguientes datos son solicitados:

![2 ventana install weblogic](/img/weblogic/2ventana-installweblogic.jpg)

**Browser** Este botón permite seleccionar el archivo .zip que contiene los binarios de instalación.

**Browser** Este botón permite seleccionar el directorio ORACLE_HOME de una instalación local de WebLogic 11g o WebLogic 12c respectivamente.

Al finalizar el proceso de instalación, la aplicación deberá ser reiniciada.

![3 confirmacion para reiniciar](/img/weblogic/3confirmacionreiniciar.jpg)

## Configuración de Plug-in “WebLogic 11g”
---

Una vez que el plugin se encuentra instalado en la aplicación, se procede a configurarlo.

*Click  Plug-Ins > Configure*

![4 menú configure](/img/weblogic/4menuconfigure.jpg)


En la siguiente pantalla se deberá seleccionar la “Aplicación y Ambiente” al cual estará asociado el Plug-in “WebLogic 11g”. Es importante conocer que una misma Aplicación” y Ambiente” pueden estar asociados a múltiples plug-ins.

![5 ventana de configuración](/img/weblogic/5ventanaconf.jpg)

En la siguiente pantalla se deberán ingresar los datos de conexión al servidor de dominio “WebLogic 11g”.

![6 datos configuración](/img/weblogic/6datosconf.jpg)

***Servidor:*** IP en donde recibe peticiones el servidor de dominio WebLogic.

***Puerto:*** Puerto en donde recibe peticiones el servidor de dominio WebLogic (Admin Server).

***Usuario:*** Usuario de conexión, este usuario deberá pertenecer al grupo de dominio WebLogic “Administrators”. 

***Password:*** Contraseña del usuario de conexión.

El proceso de conexión al servidor es iniciado, en ese momento las diferentes entradas de configuración en el servidor de dominio “WebLogic” serán descubiertas.

![7 configuracion en proceso](/img/weblogic/7confenproceso.jpg)

### Recuperación de la configuración “WebLogic”
---

En la siguiente pantalla se deberá seleccionar las entradas de configuración a descargar desde el servidor de dominio “WebLogic 11g”.

![8 Config weblogic](/img/weblogic/8Configweblogic.jpg)

***Select All*** Este botón selecciona todas las propiedades del componente de configuración seleccionado.

***Select Suggested*** Este botón selecciona las propiedades del componente de configuración sugeridas por el sistema.

> Nota: Las propiedades sugeridas por el sistema indican los campos necesarios para el proceso de aprovisionamiento de la configuración en el servidor de dominio “WebLogic”.


***Unselect All*** Este botón deselecciona todas las propiedades del componente de configuración seleccionado.

***Set as layout*** Esta opción cuando está habilitada permite guardar las entradas de configuración como plantilla, de manera que para próximas importaciones de otros ambientes se pre-seleccionen las entradas de configuraciones definidas en la plantilla.

***Import*** Este botón realiza la importación de las configuraciones seleccionadas desde WebLogic hacia Vesta.


Una vez seleccionadas las entradas de configuración el proceso de descarga de la configuración es iniciado.

![9 Descarga configuración](/img/weblogic/9Descargaconfiguracion.jpg)

### Listar entradas “WebLogic 11g”

En la siguiente pantalla se muestran las entradas de configuración provenientes de un plug-in, estas entradas son identificadas mediante iconos de color “morado”.

*Click  File > Entries*

![10 ventana entries](/img/weblogic/10ventanaentries.jpg)

### Opciones sobre entradas en plugins

Una vez que han sido definidas las entradas de plugins, se cuenta con una serie de opciones a realizar sobre ellas, estas opciones se encuentran en el menú emergente sobre la entrada seleccionada. 


### Opciones generales

Las siguientes opciones se encuentran descritas en la sección Configuración inicial > [Opciones sobre entradas](/opciones.md)

- Acquiere control
- Release control
- View entry
- Duplicate entry
- Promote entry
- Delete entry
- View children
- View History
- Tree History
- Copy Selection
- Copy property
- Compare

#### Migrate to

Esta opción permite migrar una configuración de 11g a una configuración de 12c.

*Right click  entry > Migrate to > Version to migrate*

![19 version to migrate](/img/weblogic/19versiontomigrate.jpg)


#### Push to Server (Individual)

Esta opción permite enviar la entrada de configuración seleccionada hacia el servidor de dominio “WebLogic” destino. 
Nota: Esta opción solo está disponible para “entradas de configuración” asociadas a plug-ins.

*Right Click  > Push to Server*

![20 menu push to server](/img/weblogic/20menupushtosever.jpg)

> Confirmación es requerida

![21 ventana push to server](/img/weblogic/21ventanapush.jpg)


**Start** Al presionar este botón el proceso de aprovisionamiento de la configuración es iniciado.

**Close** Este botón es habilitado una vez finaliza el proceso de aprovisionamiento de la configuración.

![22 sincronizacion completa](/img/weblogic/22sincronizacioncompleta.jpg)

Cuando una configuración no pudo ser aprovisionada en el servidor de dominio “WebLogic” manda la siguiente pantalla indicando el inconveniente:

![23 push to server](/img/weblogic/23pushtoserver.jpg)

**RollBack** Este botón es habilitado cuando una configuración no pudo ser aprovisionada en el servidor de dominio “WebLogic” permitiendo así deshacer los cambios en conflicto.


#### Resolver conflictos

Esta opción permite resolver conflictos de sincronización entre la configuración almacenada en Vesta y la configuración en el servidor “WebLogic”. Esta opción es útil cuando el envío de la configuración realizada hacia el servidor de dominio “WebLogic” no pudo comprobarse de manera automática por el sistema. Garantizando que la configuración almacenada en Vesta y la configuración del servidor de dominio “WebLogic” es concisa.


> Notas: 
> 
> Validación manual por parte del usuario dentro del servidor de dominio “WebLogic” es necesaria.
> 
> Esta opción solo está disponible para “entradas de configuración” asociadas a plug-ins.


*Right Click > Resolve Conflicts*

![24 menu resolve conflicts](/img/weblogic/24menuresolveconflicts.jpg)


Al ingresar a “Resolver Conflicts”, muestra en pantalla un mensaje preguntando si está seguro de realizar dicha acción.

![25 confirmar resolver](/img/weblogic/25confirmarresolver.jpg)

**Si** Al presionar este botón el proceso de resolución de la configuración es iniciado.
 

**No** Al presionar este botón el proceso de resolución de la configuración es cancelado.

Resultados: Cuando un conflicto es resuelto, el icono asociado a la entrada de configuración es cambiado de dirección.

![26 resolviendo conflictos](/img/weblogic/26resolviendoconflictos.jpg)

Al termino, muestra el mensaje de que se resolvió el conflicto.

![27 conflicto resuelto](/img/weblogic/27conflictoresuelto.jpg)

#### Down from Server

Esta opción permite descargar los cambios de configuración desde el servidor de dominio “WebLogic” hacia la entrada de configuración seleccionada dentro de la aplicación. 

> Nota: Esta opción solo está disponible para “entradas de configuración” asociadas a plug-ins.


*Right Click  > Down from Server*

![28 menu down server](/img/weblogic/28menudownserver.jpg)

Al seleccionar esta opción empieza cargar, una vez terminado, muestra la ventana

![29 ventana down server](/img/weblogic/29ventanadownserver.jpg)

![30 punto](/img/weblogic/30punto.jpg) Esta opción permite aceptar el cambio pendiente desde el servidor de dominio “WebLogic”.

![31 sel categoria](/img/weblogic/31selcategoria.jpg) Esta opción permite la selección de categoría. Es útil cuando se desea identificar un cambio de alta prioridad de manera visual.


> Nota: El historial de cambios sobre las entradas de configuración descargadas será actualizado de manera automática.

La siguiente pantalla muestra el resumen de cambios descargados desde el servidor de dominio “WebLogic” hacia VESTA. Los enlaces situados en la parte superior del cambio permiten la navegación a la entrada de configuración modificada.

![32 resumen de cambios](/img/weblogic/32resumencambios.jpg)

Al presionar los enlaces situados en la parte superior de la entrada de configuración se mostrará la pantalla “visualización de entradas”.

La siguiente pantalla permite visualizar las entradas de configuración descargadas desde el servidor de dominio “WebLogic”.

![33 entries de config descargadas](/img/weblogic/33entriesconfigcargadas.jpg)

#### Restore default values

Esta opción establece los valores por default de toda la entrada de configuración, los valores por default son los establecidos por el fabricante del application server.

*Right click entry > Restore default values*

![34 menu restore](/img/weblogic/34restore.jpg)


## Sincronización de Plug-in “WebLogic”
---

El proceso de sincronización es el método mediante el cual las diferentes entradas de configuración almacenadas en VESTA y las configuraciones en el servidor de dominio “WebLogic” son sincronizadas.

> Nota: Esta opción es útil cuando se desea sincronizar más de una entrada de configuración entre el servidor de dominio “WebLogic” y Vesta.

*Click Plug-Ins > Synchronize*

![35 menu syncrinize](/img/weblogic/35sincrinice.jpg)

Al ingresar a la opción de sincronización, muestra la siguiente ventana:

![36 ventana sincro](/img/weblogic/36ventanasincro.jpg)

![37 btn paloma](/img/weblogic/37btnpaloma.jpg) Esta opción selecciona la aplicación y ambiente a sincronizar.

**Push to Server** Al presionar este botón las entradas de configuración almacenados en Vesta son enviadas hacia el servidor de dominio “WebLogic”.

**Down from Server** Al presionar este botón las entradas de configuración almacenados en el servidor de dominio “WebLogic” son descargados hacia Vesta.

## Push to server

Esta opción permite enviar de manera selectiva un conjunto de configuraciones almacenadas en Vesta hacia el servidor de dominio “WebLogic”.

![38 pantalla push to server](/img/weblogic/38pantallapushtoserver.jpg)

> Nota: Esta opción es útil cuando se desea enviar un conjunto de configuraciones de manera global.

**Start** Al presionar este botón el proceso de aprovisionamiento de la configuración es iniciado.

**Close** Este botón es habilitado una vez finaliza el proceso de aprovisionamiento de la configuración.

![39 btn cmd](/img/weblogic/39btncmd.jpg)Esta opción permite la visualización del archivo log generado durante el proceso de aprovisionamiento de la configuración.

![40 ventana cmd](/img/weblogic/40ventanacmd.jpg)

### Down from server

Esta opción permite descargar de manera selectiva un conjunto de configuraciones desde el servidor de dominio “WebLogic” hacia Vesta.

![41 down from server](/img/weblogic/41downfromserve.jpg)

> Nota: Esta opción es útil cuando se desea descargar un conjunto de configuraciones de manera global. 

![37 btn paloma](/img/weblogic/37btnpaloma.jpg) Esta opción permite aceptar el cambio pendiente desde el servidor de dominio “WebLogic”.

![31 sel categoria](/img/weblogic/31selcategoria.jpg) Esta opción permite la selección de categoría. Esta opción es útil cuando se desea identificar un cambio de alta prioridad de manera visual.

La siguiente pantalla muestra el resumen de cambios descargados desde el servidor de dominio “WebLogic” hacia Vesta. Los enlaces situados en la parte superior del cambio permiten la navegación a la entrada de configuración modificado.

![42 result sincronización](/img/weblogic/42resultsincronizacion.jpg)

Al presionar los enlaces situados en la parte superior de la entrada de configuración se mostrará la pantalla “visualización de entradas”.

La siguiente pantalla permite visualizar las entradas de configuración descargados desde el servidor de dominio “WebLogic”.

![43 view children](/img/weblogic/43viewchildren.jpg)

