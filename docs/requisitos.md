# Requisitos del Sistema
---

Disponer de un equipo de cómputo para la instalación del producto considerando como mínimo las siguientes características:

-> **Generales**
---

- Contar con una licencia para la instalación de Vesta, visite la página oficial para obtener para obtener la aplicación.

- Disponer de los instaladores de Vesta, provenientes de la página oficial.

<img src="/img/instalacion/ves-chica.jpg"/>


-> **Sistema Operativo**
---

   - Microsoft Windows: como mínimo Windows XP en adelante o cualquier versión de Linux 
   - Memoria RAM: 8 GB
   - Procesador: Dual core 2 Ghz
   - Espacio en disco duro: 350 Mb de la aplicación.
   - Oracle JDK y JRE 1.8+  (no compatible con 9 o 10) o bien Oracle Linux 5.0 +, depende del Sistema Operativo con el que se disponga.
   - Winrar

![](/img/instalacion/linux-windows-hosting.png)

-> **Base de Datos**
---

   - Versión
      - Oracle DataBase 11g (Standalone o RAC)
      - Oracle DataBase 12c(Standalone o RAC)   Real aplication cluster.
     
               En caso de ser RAC se deberá disponer del componente SCAN

  - Espacio: 10 GB
  - Character Set : AL32UTF8
  - SHARED_POOL_SIZE : 147,456 KB
  - SGA_MAX_SIZE : 147,456 KB
  - DB_BLOCK_SIZE : 8 KB
  - session_cached_cursors : 100
  - processes : 500
  - open_cursors : 800
  - db_files : 600
  - Usuario: Se deberá disponer de un usuario con permisos de creación de objetos sobre la base de datos.

![](/img/instalacion/oracle_database1.jpg)