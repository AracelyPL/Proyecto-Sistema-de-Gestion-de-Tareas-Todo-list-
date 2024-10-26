Alumna: Vanessa Aracely Pérez López

Proyecto: Sistema de Gestión de Tareas(Todo-list)

Materia: Tecnologías de la Información I

Descripcion General:

El objetivo del proyecto es desarrollar un sistema de gesti´on de tareas (Todo-list) utilizando Node.js como entorno del lado del servidor, SQLite como base de datos para almacenar las tareas, y un frontend simple en HTML. El sistema permitirá a los usuarios registrarse, iniciar sesion y gestionar sus tareas.

Este proyecto cuenta con 3 clases:

index.html -> es el formulario para el registro del usuario e inicio de sesion.

En el index.html, el usuario se registr con un nombre, contraseña y correo electronico. Cuando quiere iniciar sesion, simplemente coloca el nombre de su usuario y contraseña, la cual al momento de ingresar mostrara un mensaje de "inicio de sesion exitoso" seguido de un token de autenticacion.


notas.html -> es el formulario donde el usuario puede generar una tarea, modificarla o eliminarla, incluso cuando haya cumplido la tarea la marca como completada.

Dentro de notas.html, se encuentra un pequeño formulario para la creacion de la nota o tarea a recordar, en el cual vienen los siguientes cuadros de texto: titulo, descripcion, fecha, estado, una vez que se hayan rellenado los campos antes mencionados se procede a agregar la tarea, la cual se mostrara en el apartado de "Tareas Pendientes", en dicho apartado contara con 3 botones, el boton de eliminar, editar y completado.

El boton de eliminar, como su nombre lo dice elimina la tarea de la base de datos.
El boton actualizar, hace que los datos de la tarea aparezca en los cuadros de texto correspondiente y asi poder modificarlos, para despues presionar el boton que formalmente actualizara los datos.
El boton completado, marca una tarea como "completada" y al mismo tiempo transfiere esos datos a la seccion de "Tareas Completadas", donde solo contaran con el boton de eliminar.

serverp.js -> es el en cargado de contener la base de datos llamada p1.database, la cual contiene las tablas: usuario, tareas y completada, dichas tablas estan relacionadas entre si, para asegurar que cada usuario pueda gestuiar sus propias tareas. Este script contiene los metodos CRUD (agregar, actualizar, eliminar) del archivo notas.html al mismo tiempo que los metodos para registro e inicio de sesion de los usuario del archivo index.html.

---------------------------------------------------------------------------------

Para ejecutar este programa debemos primero abrir el cmd (simbolo de sistema).
Luego, ir la carpeta en donde tenemos guardado nuestro proyecto y copiar la direccion.
Esda direccion la pegamos en nuestro cmd, antes de eso debemos agregar el siguiente comando "cd" y despues pegamos la direccion del proyecto, esto hace que la carpeta se abra dentro del cmd.
Una vez finalizado esto, procedemos a instalar las siguientes librerias que son necesarias para la ejecucion de nuestro sistema, en el cmd agregamos el siguiete comando:
npm install express bcrypt body-parser sqlite3  jsonwebtoken sequelize
Cuando las librerias esten instalas exitosamente, procedemos a ejecutar nuestro proyecto con el siguiente comando: node serverp.js
Dejamos que cargue y cuando nos aparezca en el cmd un mensaje diciendo que el servidor esta en funcion, damos click en el link que se muestra y abrira nuestra pagina.


A continuacion se muestran las siguientes imagenes de la ejecucuion del programa.

Asi se ve el registro e inicio de sesion:

![image](https://github.com/user-attachments/assets/386538d2-1002-40bc-b9b9-b0b1431950ac)

Al presionar el boton de "iniciar sesion", nos mada el siguiente mensaje:

![image](https://github.com/user-attachments/assets/335d02ab-49e9-4ec8-a062-fd3844f5eb46)

y despues aparecera el token:

![image](https://github.com/user-attachments/assets/dd79f350-2cf1-4eee-a47e-1b89fb08f2d1)

Luego podremos entrar al formulario de las tareas:

![image](https://github.com/user-attachments/assets/3b84aa85-f63e-4f50-96f4-8f0002ea6ede)

Agregamos una tarea, y al guardarla se muestra en el apartado de "Tareas Pendientes":

![image](https://github.com/user-attachments/assets/b1445a05-a379-4103-b06e-00da5830b1cd)
![image](https://github.com/user-attachments/assets/4acb54de-c166-4563-83d5-0529f850d5ce)

Cuando la tarea este completada, se muestra en el apartado de tareas completadas:

![image](https://github.com/user-attachments/assets/fe45ee5c-9965-4ffa-80f9-2a4cd7478bc7)










 


