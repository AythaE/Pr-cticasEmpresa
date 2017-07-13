# Diario
En este fichero iré recogiendo las cosas que voy haciendo diariamente para que facilite la posterior escritura de la memoria.

## 13/07/2017
Hoy por fin he logrado hacer funcionar el CRUD de instancias, los problemas de ayer se debían a que era necesario incluir los campos \_id y deleted en las validaciones de mi clase. He comenzado por tanto a recuperar la lista de instancias de AWS partiendo del código disponible en nucleoo usando boto, para ello he configurado los credenciales de aws de mi cuenta de estudiante para hacer pequeñas pruebas, con ello he añadido un método nuevo para refrescar la lista, el cual será invocado al pulsar un botón de refresco, no he tenido tiempo para testearlo completamente aún y por ahora solo añadiría a la BD las instancias recuperadas de AWS.
