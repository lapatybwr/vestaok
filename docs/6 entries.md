# Entries
---

Las entradas representan las configuraciones de los componentes que se desean gestionar y han sido definidos dentro de las aplicaciones. 
Las entradas están representadas por un grupo de aplicación que a su vez contiene una o varias aplicaciones con ambientes definidos y dentro de cada ambiente se encuentran los componentes con las configuraciones de las entradas.

**Click  File > Entries**

![Menu entries](/img/entries/1menuentries.jpg)


## Agregar entradas
---

Las entradas son almacenadas en un componente que se encuentran bajo un ambiente de trabajo definido dentro de una aplicación dentro un grupo determinado.

En la siguiente ventana se muestran las diferentes entradas de configuración ya asociadas a una aplicación, estas entradas de configuración están asociadas a su vez a un ambiente y son definidas mediante la asignación de valores a las diferentes propiedades de un componente. 

![Pantalla de entries](/img/entries/2agregaresntries.jpg)


Al ingresar a la ventana de entries por primera vez, aparecerá vacía porque aún no se han definido las entradas para las aplicaciones.

 
![Imagen de refresh y datos](/img/entries/bton-mas.jpg)Por medio de este botón se mostrara una ventana que contiene los diferentes componentes de configuración disponibles, de la lista desplegable se elige el componente:

![Boton mas](/img/entries/3selec-comp.jpg)


Una vez seleccionado el componente, se ingresarán los diferentes valores para la creación de la entrada de configuración. 

Entre los valores obligatorios se encuentra como primera validación la selección de la aplicación y posteriormente el ambiente al cual estará asociada la entrada de configuración.

![Seleccionar componente de entrada](/img/entries/4crear-newentri.jpg)


Los valores de las entradas tipo “Cadena de texto” son mostradas de manera normal, como texto.
Los valores de entradas tipo “Contraseña” son mostradas de modo protegida 
Los valores de entradas tipo “Componente” son representadas por un icono cuadrangular, el cual podrá ser seleccionado para listar las entradas del componente anidado.


> Nota: Es posible asignar una “categoría” para cada propiedad asociada a la entrada de configuración.

El botón “Show Category” muestra las diferentes categorías disponibles en cada propiedad. Esta opción es útil cuando se desea identificar una propiedad con un grado de prioridad alta, normal o baja.

![Crear entrada](/img/entries/5show-category.jpg)


Existen configuraciones, que por su naturaleza son difíciles de manejar en un solo componente de configuración, por lo tanto es posible definir componentes que contengan referencias a otros componentes, en este caso, al crearse una entrada de este tipo, es necesario ingresar valores a las diferentes propiedades de cada componente.

Una vez creada la entrada, se muestra en la pantalla los elementos que la componen.

![Imagen show category](/img/entries/6entries.jpg)


Cuando las entradas han sido ingresadas, la ventana cuenta con una serie de acciones y elementos que se describen a continuación:

**Refresh**. 
La aplicación tiene dos opciones para refrescar la vista de entradas de configuración.
Manual: Usando el botón de “refresh”. Para aplicar la actualización de la vista con lo último guardado en base de datos.

***Manual***: Usando el botón de “refresh”. Para aplicar la actualización de la vista con lo último guardado en base de datos.

***Automática***: El sistema automáticamente se va actualizando de acuerdo con los parámetros establecidos. Ver sección de System Parameters del menú Administration.

![Elementos de entries](/img/entries/7-0menurefresh.jpg)


Modifique los parámetros de sistema para configurar el “refresh” automático de la vista de entradas de configuración.


![Imagen de loading](/img/entries/7-1loading.jpg) Es el tiempo que tardó la vista en refrescarse sin importar si el “refresh” fue manual o automático.

![Imagen de last](/img/entries/7-2last.jpg) Es la fecha hora de la última vez que se refrescó la vista sin importar si el “refresh” fue manual o automático.

![Imagen de next](/img/entries/7-3next.jpg) Es la fecha hora del próximo “refresh” automático. Se calcula con base en el parámetro de sistema: “Time in which the entries will be updated” medido en segundos.

### Opciones sobre entradas
---

Una vez que se tienen establecidas las entradas, se tiene una serie de opciones a realizar sobre ellas, siempre y cuando se tenga el perfil de usuario con los permisos adecuados. 

#### Create entry
---

Las entradas de configuración son los valores que son ingresados a la aplicación en forma de registros y se les denomina propiedades. 

**Select “Common” > Right click > Create entry**

![Crear entrada menu contextual](/img/entries/8crearentries.jpg)


![Signo mas](/img/entries/bton-mas.jpg)Esta opción permite crear una entrada de configuración desde un ambiente en específico. También puede crearse la entrada desde el menú emergente del ratón.

Asigne valores a las propiedades y guarde con el botón **“Save”**.

![Valores de entradas](/img/entries/9create.jpg)



#### Acquire control
---

Permite tomar el control de la entrada para poder tomar acciones sobre ella sin que otro usuario pueda modificarla mientras se encuentre utilizando. Esta opción es importante mencionar y resaltar que es útil ya que permitirá la manipulación de los elementos registrados, sin esta acción no se tendrán habilitadas las funciones.

**Right Click  > Acquire control**

![Menpu con acquire ctrl](/img/entries/10acquiere.jpg)

Una vez que se adquiere el control, se habilitan las acciones sobre las características del elemento.

![Acquire control](/img/entries/10acquiere2.jpg)

#### Release control
---

Permite ceder el control adquirido de la entrada para que otros usuarios puedan hacer uso de ella.

**Right Click  > Release control**

![Menú release ctrol](/img/entries/11-release.jpg)


#### Edit entry
---

Esta opción permite visualizar y editar los valores de una entrada de configuración.

> Nota: Se requiere adquirir el control de la entrada previo a editar o eliminarla.

**Right Click  > Edit Entry**

![Menú edit entry](/img/entries/12-edith.jpg)


Los valores actuales de la entrada de configuración son mostrados, además es posible asignar nuevos valores y/o definir categorías oprimiendo el botón “Show Category”

![Ventana edit entries](/img/entries/12-edithentri2.jpg)


Donde se permite seleccionar la categoría en cada propiedad. Esta opción es útil cuando se desea identificar una propiedad de alta prioridad de manera visual.

![Imagen hide category](/img/entries/13-showcategori.jpg)

#### Duplicate entry
---

Esta opción permite duplicar una entrada de configuración en un aplicativo alterno o bien realizar una copia local.

**Right Click  > Duplicate Entry**


![imagen dulicate entry](/img/entries/14-duplicar.jpg)

La siguiente pantalla muestra la entrada duplicada, en la cual se puede seleccionar en cual aplicación estará asociada la nueva entrada de configuración. Sin embargo el ambiente ya se encuentra definido de acuerdo con la configuración inicial del elemento original del que se duplico.

![Pantalla con entrada duplicada](/img/entries/15-duplientri.jpg)

> Nota: Para duplicar la “entrada de configuración” en la misma aplicación solo es necesario indicar los nuevos valores de cada una de las propiedades y guardar con el botón “Save”

#### Promote entry
---

Esta opción permite promover una entrada de configuración hacia un ambiente subsecuente. Esta opción es útil cuando una metodología de integración continua es utilizada.

> Nota: Esta opción es muy útil cuando se requiere la propagación de configuraciones entre ambientes.

**Right Click  > Promote Entry**


![menu promote entry](/img/entries/16-promote.jpg)


Esta opción permite elegir el ambiente al cual estará asociada la entrada de configuración a promover.

![Elegir ambiente](/img/entries/17-promEnriron.jpg)

#### Delete entry
---

Esta opción permite eliminar una entrada de configuración.

> Nota: Este proceso requiere confirmación por parte del usuario.


Se requiere adquirir el control de la entrada previo a editar o eliminar la entrada.

**Right Click  > Delete entry**

![menu delete entry](/img/entries/18-delete.jpg)

Antes de eliminar el elemento seleccionado, valida si está seguro de eliminarlo

![confirmación](/img/entries/18-deleteconfirm2.jpg)


Al presionar el botón “Si” la entrada de configuración es eliminada.

Al presionar el botón “No” el proceso de eliminación, no se realiza.


#### View children
---

La siguiente pantalla muestra las diferentes entradas de configuración anidadas y asociadas a la entrada de configuración principal.

**Right Click  > View Children**

![menú view children](/img/entries/19-viewchildren.jpg)

Esta pantalla permite agregar, modificar, o eliminar “entradas” de configuración del tipo componente anidado.

![ventana de view children](/img/entries/19-viewchildren2.jpg)

![signo mas](/img/entries/bton-mas.jpg) Este botón permite agregar una entrada de configuración del tipo seleccionado.

> Nota: para poder hacer uso de la opción “View Children, se debe tener una asociación hacia otro componente por medio de una configuración de tipo “Bean”


#### View history
---

La siguiente opción muestra el historial de cambios realizados sobre los valores de una “entrada de configuración” específica.

**Right Click > View History**

![ventana de los view history](/img/entries/20-view-history.jpg)

La siguiente pantalla muestra los cambios de valores sobre las entradas de configuración mediante una visualización basada en colores, siendo el color verde el registro original y el color azul los registros cambiantes.


![menú view history](/img/entries/21-entrihistory.jpg)


####Tree history
---

En la siguiente opción se muestra el historial de cambios realizados sobre una “entrada de configuración” específica basada en las revisiones existentes.

> Nota: Esta opción es útil cuando se desea identificar una configuración errónea y regresar a una configuración estable.

**Right click  > Tree history**

![menu tree history](/img/entries/22-treehistory.jpg)

Se muestran las revisiones de la entrada de configuración, una revisión se genera cada que se modifica la entrada de con

![ventana tree history](/img/entries/23-entrihistory.jpg)

Doble click sobre el registro de la revisión que se desea saber la información que cambió. 

La siguiente pantalla muestra los cambios de valores de las “entradas de configuración” mediante una visualización basada en colores:

![cambios de valores](/img/entries/24-treehistory.jpg)

Al final de la ventana se encuentran acciones a realizar: 

**Show Blanks:** Esta opción permite mostrar las entradas con propiedades en blanco.

**Show all:** Esta opción permite mostrar todas las entradas.

**Export to excel:** Esta opción permite exportar a Excel para tener un reporte de cambios.

![archivo de excel](/img/entries/25-excel.jpg)

**Revert Changes:** Esta opción permite sobrescribir los valores actuales de una entrada de configuración con los valores de la revisión seleccionada. La que se encuentre activa en “Revert Change” 


#### Copy Selection
---

Esta pantalla permite copiar al portapapeles las entradas de configuración seleccionadas, será necesario crear una selección de la “entrada” con el mouse o con las teclas [Shift + Dirección].

**Right Click  > Copy selection**

![menú copy selection](/img/entries/27-copyselection.jpg)


> Nota: Esta opción es útil cuando se requiere compartir información con usuarios externos a VESTA.


#### Copy Property
---

Esta pantalla permite copiar al portapapeles el valor de una entrada de configuración en específico. 

*Right Click  > Copy Property > Name*

![menú copy property](/img/entries/28-copyproperty.jpg)

> Nota: Esta opción es útil cuando se requiere copiar datos de URL’s o credenciales de acceso.

#### Compare
---

Esta opción permite comparar entradas de configuración del mismo tipo.

*Right Click  > Compare> Other proerty values*

![menú compare other proerty](/img/entries/29-compare.jpg)

Al seleccionar la comparación, muestra el resultado obtenido

![resultado de compare](/IMG/ENTRIES/30-comparecomp.JPG)

Al final de la ventana se encuentran acciones a realizar: 

**Show Blanks:** Esta opción permite mostrar las entradas con propiedades en blanco.

**Show all:** Esta opción permite mostrar todas las entradas.

**Export to excel:** Esta opción permite exportar a Excel para tener un reporte de cambios.

![archivo de excel](/img/entries/31-excel.jpg)

### Opciones sobre los ambientes
---

Existe una serie de acciones que se realizan sobre los ambientes que fueron definidos. Para acceder a ellos, dar clic derecho sobre el ambiente y muestra todas las opciones.

Las opciones varían de acuerdo con las configuraciones que se hayan establecido dentro de cada uno, por ejemplo, si ya se encuentra configurado sobre un ambiente los dos plugin: weblogic y soa, se mostraran más opciones para trabajar sobre ellos.

![menu opciones](/img/entries/opc-environ/1opc-envirn.jpg)

Si solo tiene un plugin configurado, solo muestra lo que se puede hacer con él.

![opciones de configuración con plugin](/img/entries/opc-environ/1opc-environ2.jpg)

Si aún no tiene configurados ningún plugins, solo muestra las opciones para poder configurarlo.

![opciones de config sin plugin](/img/entries/opc-environ/1opc-environ3.jpg)

#### Compare environment
---

Compara ambientes permite comparar las entradas de configuración de dos ambientes distintos con el fin de identificar diferencias de configuración entre ambos ambientes.

> Nota: Esta opción es útil cuando se tiene conflicto de configuraciones entre ambientes y se desea identificar una versión concreta de la configuración.
 
*Right Click  Environment >Compare environment with > “Environment name”*

![menu compare environment whit](/img/entries/opc-environ/2compare.jpg)


La siguiente pantalla muestra la comparación de las entradas de configuración de los ambientes seleccionados.

![ambientes comparados](/img/entries/opc-environ/3verde.jpg)


Muestran las entradas de configuración existentes en el ambiente principal y que se encuentran ausentes en el ambiente secundario sobre el cual se está realizando el proceso de comparación.

![testing environment](/img/entries/opc-environ/4rojas.jpg) Muestran las entradas de configuración existentes en el ambiente secundario que se encuentran ausentes en el ambiente principal.

![testing 30](/img/entries/opc-environ/5azul.jpg) Muestra la diferencia entre los valores dentro de una entrada de configuración entre ambientes.

![compare environments](/img/entries/opc-environ/6todo.jpg)

Al final de la ventana se encuentran acciones a realizar: 

**Show Blanks:** Esta opción permite mostrar las entradas con propiedades en blanco.

**Show all:** Esta opción permite mostrar todas las entradas.

**Export to excel:** Esta opción permite exportar a Excel para tener un reporte de cambios.


#### Show categories
---

Esta opción permite mostrar las entradas de configuración de determinada categoría o puedes elegir mostrar todas.

*Right Click  Environment> Show category > category name*

![imagen menu ctegory name](/img/entries/opc-environ/7show-categ.jpg)

Utilice la lista de categorías para cambiar la información se debe mostrar

![imagen menu ctegory name](/img/entries/opc-environ/8pant-show.jpg)



#### Compare categories with
---

Esta opción permite comprar las categorías de las entradas de configuración de un ambiente contra las de otro ambiente de la misma aplicación.

*Right Click  Environment> compare category with> Environment name*


![Lista de categorias](/img/entries/opc-environ/9comp-categ.jpg)


![menú compare with](/img/entries/opc-environ/10pant-comp.jpg)


**Export to Excel** Esta opción permite exportar las diferencias de categorías a Excel para tener un reporte de cambios.

![archivo excel](/img/entries/opc-environ/11excel.jpg)

#### Tree history
---

Esta opción permite ver el historial de cambios que ha tenido el ambiente

*Right Click ENVIRONMENT> Tree history*

![menu tree history](/img/entries/opc-environ/12tree-history.jpg)

Aparece el listado de revisiones de cambios que ha tenido el ambiente.

![listado de revisiones](/img/entries/opc-environ/13entry-history.jpg)

Doble click en una revisión para ver las diferencias que tiene con los valores actuales.

![diferencias con valores actuales](/img/entries/opc-environ/14pant.jpg)

Al final de la ventana se encuentran acciones a realizar: 

**Show Blanks:** Esta opción permite mostrar las entradas con propiedades en blanco.

**Show all:** Esta opción permite mostrar todas las entradas.

**Export to excel:** Esta opción permite exportar a Excel para tener un reporte de cambios.

![archivo excel](/img/entries/opc-environ/15excel.jpg)

**Revert changes** Seleccionando una revisión en específico y al dar click  en “Revert changes” se dará “revert” a los cambios actuales y se tomarán como actuales los cambios de la revisión seleccionada.


#### Export environment 
---

Esta opción permite exportar las entradas de configuración almacenadas en una aplicación seleccionada en un formato HTML que permite la personalización visual de los elementos de configuración para su posterior impresión. 

*Right click  environment> Export environment*

![manú export envirnment](/img/entries/opc-environ/16export-environ.jpg)

Se genera una vista HTML que se abre en el navegador web que se tenga configurado por default.

![ventana página web](/img/entries/opc-environ/17html.jpg)

#### Export environment TO EXCEL FILE
---

Esta opción permite exportar las entradas de configuración de una aplicación seleccionada en un formato XLS que permite la personalización visual de los elementos de configuración para su posterior impresión. 

**Right click  environment> Export environment as Excel file**

![menú export as excel](/img/entries/opc-environ/18export.jpg)

Se genera un reporte en formato XLS que puede abrirse después con Excel

![archivo excel](/img/entries/opc-environ/19excel.jpg)






