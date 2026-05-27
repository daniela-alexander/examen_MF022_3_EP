# EJERCICIO 1 - 

## ERRORES DETECTADOS Y SOLUCIONES
La red tiene nombres diferentes:

* ```net_devXX```
* ```net_dev_XX```

En el servicio ```srv_dev_XX```, declaramos que queremos usar la red net_devXX (sin guion bajo entre 'dev' y 'XX'). Pero abajo del todo, en networks, la red se llama net_dev_XX (con guion bajo entre 'dev' y 'XX'). Por lo tanto, cuando ejecutamos el comando docker-compose up, Docker Compose se quejará de que la red ```net_devXX``` no está definida, porque en realidad la red que hemos definido se llama ```net_dev_XX```.

    ❌networks:
      - net_devXX
    


Para solucionar este error, debemos asegurarnos de que el nombre de la red sea consistente en todo el archivo docker-compose.yml. Es decir, si decidimos llamar a la red net_dev_XX, entonces debemos usar ese mismo nombre en el servicio srv_dev_XX. De esta manera, Docker Compose podrá encontrar la red correctamente y no se producirá ningún error al ejecutar el comando docker-compose up.

    ✅networks:
      - net_devXX


Otro de los errores es el uso de la imagen. Aquí utilizamos ```ubuntu:22```, por lo que el contenedor de Ubuntu no tiene ningún servicio activo corriendo en segundo plano que mantenga el contenedor en ejecución. Por lo tanto, cuando ejecutamos el comando docker-compose up, el contenedor se iniciará y luego se detendrá inmediatamente porque no hay ningún proceso en ejecución que lo mantenga activo. 

    ❌image: 
        ubuntu:22
    
    ✅image:
        ubuntu:22.04

> Es mejor usar ```ubuntu:22.04```para que Docker pueda encontrar la imagen correcta en el repositorio de Docker Hub.

Para solucionar este error, debemos asegurarnos de que el contenedor tenga un proceso en ejecución que lo mantenga activo. Por ejemplo, podríamos agregar un comando como ```"tail -f /dev/null"``` al final del ```servicio srv_dev_XX``` para mantener el contenedor en ejecución. De esta manera, cuando ejecutemos el comando ```docker-compose up```, el contenedor se iniciará y permanecerá activo hasta que decidamos detenerlo manualmente.

    ✅command: "tail -f /dev/null"