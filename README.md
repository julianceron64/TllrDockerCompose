## DESARROLLO DEL PROYECTO

Despues de hacer las modificaciones solicitadas en clase podemos ver que el ejercicio ya no funciona, a continuación se puede ver una imagen que muestra que el metodo GET, en 
este caso desde el buscador retorna un error
![Texto alternativo](https://github.com/julianceron64/TllrDockerCompose/blob/main/Captura%20de%20pantalla%202025-09-15%20224632.png?raw=true)

Así mismo, en la siguiente imagen podemos ver que el metodo POST tambien lanza un error
![Texto alternativo](https://github.com/julianceron64/TllrDockerCompose/blob/main/Captura%20de%20pantalla%202025-09-15%20230417.png?raw=true)

## CONCLUSIONES

Durante el desarrollo del proyecto se presentó una situacion en la que el programa funcionaba cuando no debia ser asi, después de consultar con el docente el porque sucedía
esto, se hizo un cambio al docker-compose, en el cual, en lugar de remover por completo todas las menciones a network, se añadió "network_mode: bridge" a cada servicio, 
con el fin de especificar que la conexión debia de ser tipo bridge, y "remover" una posible configuración en los hosts de cuando se corrió la version que definía las redes, 
después de hacer este cambio, el programa dejo de funcionar, el cual era el fin del taller

Con este taller se pudo comprobar que es importante hacer uso de user-defined bridges, para facilitar las conexiones mediante usos de DNS, pues permite que el programa 
funcione con el nombre del servicio, sin necesidad de memorizar y poner direcciones IP
