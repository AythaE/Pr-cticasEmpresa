# Diario
En este fichero iré recogiendo las cosas que voy haciendo diariamente para que facilite la posterior escritura de la memoria.

## 03/07/2017
Primer día, instalación de diversas herramientas e intentos de despliegue en docker con problemas por falta de base de datos y acceso a repositorios.

## 04/07/2017
Arreglado despliegue de docker, realizado la primera aportación el repositorio base2 con la documentación actualizada para desplegar el en docker

## 05/07/2017
He estado haciendo el tutoral de AngularJS 1.x <https://www.codeschool.com/courses/shaping-up-with-angularjs> el cuál he subido a un repo propio de gitlab. En el daily scrum se me asignó llevar a cabo un CRUD de otro elemento sobre el repositorio base2 a modo de entrenamiento. Intenté comenzar pero el tutorial me llevó algo más de tiempo del esperado así que comenzaré mañana con ello.

## 06/07/2017
He estado intentando crear un CRUD a partir de RestItem sobre el repositorio base2, de igual manera que se realiza con usuarios. Estoy teniendo algunos problemas para comprender el código debido a que incluye bastantes cosas y a que no puedo realizar pruebas sin desplegar toda la aplicación. Sobre la aplicación he estado probando a crear usuarios pero se produce un error tras introducir el Email, lo que impide que pueda ver como se añaden usuarios. He creado el esqueleto de una clase Ec2Instance apartir del de usuario, pero debería de probar como funciona antes usuarios.

## 10/07/2017
Hoy he continuado con el CRUD de instancias AWS sobre el proyecto Bat. He tenido diversos problemas con la api de usarios que no me ha permitido ver en funcionamiento el alta y modificación de estos. Aún así he creado una rama en dicho proyecto, llamada crud_ec2instance en la que he añadido la parte correspondiente al backend de este CRUD aunque no esté totalmente operativa aún. Para probar las apis he estado usando la herramienta Postman logrando hacer algunas pruebas con la api de usuarios.

## 11/07/2017
He estado instalando y jugando el la rama LabDay del repositorio de APM ya que lleva un ejemplo de aplicación más simple que el de usuarios lo que me ha ayudado a entender la lógica de rest_item. He estado teniendo problemas para realizar peticiones post usando postman, probablemente debido al token csrf, pero he encontrado la herramienta postman interceptor que permite redirigir las peticiones a postman, con ello podre copiar los headers de un post hecho desde la UI web y poder realizar el testeo de mi API, también he estado modificando algunas cosillas que no eran necesarias de mi clase pero que inicialmente añadí por estar en usuarios sin entender muy bien como funcionaba.

## 12/07/2017
Hoy he logrado testear en postman adecuadamente, he sido añadido en jira y tengo asignada mi primera tarea del listado de instancias. Sigo teniendo problemas para hacer funcionar mi backend de instancias a pesar de haberlo simplificado tras haber aclarado algunos conceptos en el daily scrum de hoy. En concreto estoy teniendo un problema para insertar usando services.py de apm donde se produce un error 400 con el mensaje "extra keys not allowed"

## 13/07/2017
Hoy por fin he logrado hacer funcionar el CRUD de instancias, los problemas de ayer se debían a que era necesario incluir los campos \_id y deleted en las validaciones de mi clase. He comenzado por tanto a recuperar la lista de instancias de AWS partiendo del código disponible en nucleoo usando boto, para ello he configurado los credenciales de aws de mi cuenta de estudiante para hacer pequeñas pruebas, con ello he añadido un método nuevo para refrescar la lista, el cual será invocado al pulsar un botón de refresco, no he tenido tiempo para testearlo completamente aún y por ahora solo añadiría a la BD las instancias recuperadas de AWS.
