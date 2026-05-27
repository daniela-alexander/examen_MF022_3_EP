# EJERCICIO 3
## Explicación del problema

El problema es causado por procesos que consumen CPU, memoria y disco, lo que hace que el sistema se vuelva lento e inestable. Para solucionar este problema, es necesario identificar los procesos que están consumiendo recursos y tomar medidas para reducir su impacto en el sistema.

## Solución propuesta

- Ver consumo CPU
  
 ```top```

- Ver procesos
  
  ```ps aux```

- Ver consumo memoria
  
  ```free -h```

- Ver consumo disco
  
  ```df -h```

El problema lo esta causando el comando ```yes > dev/null```, el cual esta consumiendo el 100% de la CPU. El comando ```yes``` genera texto infinito y se ejecuta en segundo plano. Para solucionar el problema, se puede matar el proceso utilizando el comando ```kill``` seguido del PID del proceso. Por ejemplo:

```kill <PID>```

El comando ```cat /dev/zero | head -c 300M > /tmp/mem_test1 &
cat /dev/zero | head -c 300M > /tmp/mem_test2 &``` está consumiendo memoria, ya que está generando archivos de 300 MB cada uno, saturando RAM y swap. Para solucionar este problema, se pueden eliminar los archivos generados utilizando el comando ```rm``` seguido del nombre del archivo. Por ejemplo:

```rm /tmp/mem_test1```

El disco se encuentra saturado debido al comando ``` for i in {1..30}
do
dd if=/dev/zero of=/tmp/test_disk/file_$i bs=1M count=5
done ```, el cual está generando archivos de 5 MB cada uno, saturando el espacio en disco. Para solucionar este problema, se pueden eliminar los archivos generados utilizando el comando ```rm``` seguido del nombre del archivo. Por ejemplo:

```rm /tmp/test_disk/file_1```

## Conclusión
En conclusión, para solucionar el problema de consumo de recursos en el sistema, es necesario identificar los procesos que están causando el problema y tomar medidas para reducir su impacto. Esto puede incluir matar procesos que consumen demasiada CPU, eliminar archivos que consumen demasiada memoria o espacio en disco, y monitorear regularmente el uso de recursos para evitar futuros problemas.

## Comandos utilizados
            1  #!/bin/bash
            2  yes > /dev/null &
            3  cat /dev/zero | head -c 300M > /tmp/mem_test1 &
            4  cat /dev/zero | head -c 300M > /tmp/mem_test2 &
            5  mkdir -p /tmp/test_disk
            6  for i in {1..30}; do  dd if=/dev/zero of=/tmp/test_disk/file_$i bs=1M count=5; done 
            7  top
            8  htop
            9  ps aux
        10  ps aux | grep yes
        11  free -h
        12  df -h
        13  du -sh /tmp/*
        14  yes > /dev/null
        15  pkill yes
        16  rm -f /temp/mem_test1
        17  rm -f /temp/mem_test2
        18  rm -f /temp/test_disk
        19  sudo sync
        20  sync
        21  sysctl -w vm.drop_caches=3
        22  top
        23  free -h
        24  df -h