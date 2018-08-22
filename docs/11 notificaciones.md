# Notificaciones

Las notificaciones son envíos de mensajes a la aplicación Vesta cuando se han realizado cambios en la consola del servidor weblogic. son una parte fundamental en la aplicación ya que avisa cuando algún usuario realizo alguna modificación a los valores contenidos en la aplicación.

*Click > Notification*


<img src="/img/notificaciones/1menunotificacion.jpg"/>


Cuando un cambio es realizado inmediatamente manda una ventana emergente a la aplicación Vesta notificando el cambio en la consola del servidor de weblogic.


![IMG](/img/notificaciones/2pantalla.jpg)



La ventana cuenta con acciones a realizar sobre el cambio realizado:

| Acción | Descripción |
|---------------|------------------------------------------------------------------------------------------------------|
| Accept all	| Acepta los cambios realizados en el servidor weblogic y se aplican en Vesta                          |
| Rollback all | Rechaza los cambios realizados en el servidor weblogic y se queda con los valores originales de Vesta |
| Discard all | Descarta los cambios realizados en el servidor de weblogic.                                            |
| Ignore | Ignora el mensaje enviado para que el usuario que realizo el cambio pueda continuar con la modificación.    |
| Boton candado | Este botón debe ser activado para que permita realizar alguna de las acciones mencionadas: Accept all, Rolback all, Discard all. |


