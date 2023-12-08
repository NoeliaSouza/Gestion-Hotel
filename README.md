# Proyecto de sistema de gestión - Reservas de hotel

UTN FRGP - Laboratorio de Computación II

Integrantes:

- Afonso de Souza, Noelia
- Alduncin, Joaquín
- Felice, Pablo


------------
## Introducción:
-------------
El sistema consiste en gestionar las reservas de un hotel.
Para esto cuenta con un menú principal y una serie de submenúes que serán la interfaz gráfica para la gestión de los clientes, las reservas, los ingresos por reservas, los usuarios del programa y las habitaciones con las que cuenta el hotel.

![1-Menu principal](https://user-images.githubusercontent.com/122423086/212205971-6054e61b-46b7-44a1-8472-9835eb11b90a.JPG)



-----------------------------
## Descripción detallada del sistema: 
-----------------------------

### Usuarios e ingreso al sistema 
Para poder ingresar el sistema nos pide un usuario y contraseña. Si es la primera vez que se utiliza el programa, el sistema solicita que se cree el primer usuario ADMIN, el cual, entre otras opciones, va a poder registrar a otros usuarios (ya sean empleados u otros ADMINS). Para ello nos pide datos tales como numero de legajo, nombre, apellido, etc: 

![Registrarse](https://user-images.githubusercontent.com/122423086/212206027-d832b16b-ba46-413f-97c8-ac9c37cdd0f6.JPG)




Una vez ingresado al sistema, dentro del menú secundario encontramos opciones que van a estar disponibles según el nivel de acceso del usuario en ese momento. En la cabecera del menú secundario se detallan los datos del usuario logueado:

![2-Menu secundario](https://user-images.githubusercontent.com/122423086/212206081-faf03869-6c78-476e-9ee1-b2ab08c80f7e.JPG)


### Reservas

Ingresando al submenú “Realizar reserva” el sistema nos pedirá una fecha de ingreso de estadia y una fecha de egreso de estadia, para poder mostrar por sistema las habitaciones disponibles en los días solicitados. El cliente  podrá elegir la habitación dependiendo de la disponibilidad del momento y de la cantidad de personas que sean, ya que el hotel cuenta con diferentes tipos de habitaciones (1-simple, 2-dobles, 3-triples). En el caso de que las habitaciones se encuentren disponibles, el sistema las mostrara en color "verde":

![3-Hacer reserva](https://user-images.githubusercontent.com/122423086/212206107-c2062378-dbd5-4619-b059-bc8c276964d0.JPG)



En el caso de que exista una habitación ocupada en la fecha solicitada, el sistema mostrara la misma en color “rojo”.:

![3-Hacer reserva 3 ocupados](https://user-images.githubusercontent.com/122423086/212206120-5732ac50-43a2-415c-a88a-cfa4fcb46db3.JPG)



Una vez el sistema emita por pantalla las habitaciones disponibles,  solicitará el ingreso de la habitación elegida (solo se podrán elegir las habitaciones que están como “disponibles en color verde”, en el caso de elegir una ocupada el sistema lo tomara como incorrecto y pedirá que se ingrese una habitación valida).
Luego de elegir el numero de habitación, el sistema solicitará el DNI del cliente. En el caso de que el cliente ya exista en los archivos, mostrará los datos del mismo por pantalla y se pasara al detalle de la reserva (total de días, total a abonar, medio de pago, etc).
Si el DNI del cliente no se encontrara en los archivos, entonces el sistema pedirá los datos del mismo (apellido, nombre, fecha de nacimiento, mail y telefono). Luego, se guardará el cliente en un archivo y se procederá a mostrar los datos de la reserva. 

Una vez colocado el método de pago, se oficializa la reserva y la habitación pasa de desocupada a ocupada, por lo cual no podrá reservarse en la misma fecha por otra persona.


![3-Hacer reserva 2 pide datos](https://user-images.githubusercontent.com/122423086/212206136-1b373b9c-8f86-41cd-b8fa-bdd6b4cb0656.JPG)


Es posible generar hasta 3 reservas con el mismo DNI para la misma fecha de ingreso. Si se quisiera realizar una 4ta reserva, el sistema emitirá un cartel comunicando que no es posible, ya que se supero el limite de reservas. Este limite se estableció con el fin de prevenir que un solo cliente realice varias reservas  y  luego no se haga presente, dejando varias habitaciones inhabilitadas para que otros clientes las ocupen.

![3-Hacer reserva 3 supero limite](https://user-images.githubusercontent.com/122423086/212206148-5aa42785-9b8a-4597-9e79-101d3b9cb88b.jpg)


### Nivel de acceso y permisos de usuario

Según el nivel de acceso que posea el usuario, se podrá acceder o no a algunas opciones del submenú, como por ejemplo, modificar los precios de habitaciones, modificar datos de otros usuarios en el sistema, realizar copia de seguridad, restaurar copia de seguridad, etc.

![8-Permisos admin 2](https://user-images.githubusercontent.com/122423086/212206168-e323ccdc-4c7a-4d31-8a31-062b34de58d9.jpg)


A su vez, el sistema emitirá por pantalla si el legajo ingresado no existe o la contraseña ingresada es incorrecta.

![8-Permisos admin 3 no existe legajo](https://user-images.githubusercontent.com/122423086/212206182-37326496-598d-4e62-8b5e-a22340240ea4.jpg)



![8-Permisos admin](https://user-images.githubusercontent.com/122423086/212206430-8398b5be-fe84-428f-af18-9c9d5664ffa4.JPG)



### Consultar reservas y disponibilidad
La opción 4 del submenú permite consultar reservas en base a un número de DNI o en base a un numero de reserva.



![4-Consultar reserva](https://user-images.githubusercontent.com/122423086/212206223-20a8531a-6289-46a7-83e0-d742a834bd54.JPG)



La opción 5 del submenú permite consultar disponibilidad entre 2 fechas dadas. El sistema emite un listado de fechas ocupadas en color "rojo" y desocupadas en color "verde" de cada habitación, según el mes consultado:

![5-Disponibilidad](https://user-images.githubusercontent.com/122423086/212206233-0fe0f0e0-bad0-4428-9271-53e9a196f10b.JPG)



### Informes
En el submenú “Informes” se podrán consultar informes anuales relacionados a la recaudación, ya sea anual general, por cliente, o por habitación.




![6-Informes](https://user-images.githubusercontent.com/122423086/212206257-f758debc-fff2-436b-bd85-bd7271f7ed9d.JPG)


![6-Informes 2](https://user-images.githubusercontent.com/122423086/212206652-8bc44a24-4c8e-46ec-82da-a51cdef917e1.JPG)


![6-Informes 3 clientes](https://user-images.githubusercontent.com/122423086/212206284-4f36565c-8a2d-455f-9166-dca14c583d03.jpg)

![6-Informes 4 habitacion](https://user-images.githubusercontent.com/122423086/212206289-b8d0c655-ae28-45b2-a1a1-87077e6e7900.jpg)


### Listados
El submenú “Listados” muestra la cantidad de habitaciones que hay,la cantidad de usuarios, clientes, y reservas. 


![7-Listados](https://user-images.githubusercontent.com/122423086/212206317-c435635e-fb38-4528-8481-e60db6e46371.JPG)

![7-Listados 2](https://user-images.githubusercontent.com/122423086/212206313-5fc54806-5892-405c-bd7c-7f8ac2af1337.jpg)




--------------
## UML
--------------

![Diagrama de Clases UML](https://user-images.githubusercontent.com/122423086/211724483-854f2eab-f469-426b-844e-b66bc7cf753f.JPG)


Se utilizó C++, POO, clases, herencia, composición, archivos binarios, memoria dinámica para la generación de reservas, ventas y clientes, etc.



