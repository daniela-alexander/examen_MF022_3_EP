# # Proyecto MF0223 - Ejercicios Prácticos

Este repositorio contiene los ejercicios prácticos realizados. A continuación, se describen los ejercicios y las soluciones implementadas en cada carpeta.

---

## Contenido del repositorio

### 1. [MF0223_3_EP_01_Alexander_Daniela](MF0223_3_EP_01_Alexander_Daniela/)
#### Ejercicio 1: Configuración de Docker Compose

En este ejercicio, se trabajó con un archivo `docker-compose.yml` para configurar un contenedor basado en Ubuntu. Se detectaron y corrigieron los siguientes errores:

- **Inconsistencia en los nombres de la red:** Se corrigió el nombre de la red para que sea consistente en todo el archivo.
- **Versión de la imagen:** Se actualizó la imagen de `ubuntu:22` a `ubuntu:22.04` para evitar problemas de compatibilidad.
- **Mantener el contenedor activo:** Se agregó el comando `tail -f /dev/null` para evitar que el contenedor se detenga inmediatamente después de iniciarse.

Archivo relevante:
- [docker-compose.yml](MF0223_3_EP_01_Alexander_Daniela/docker-compose.yml)

---

### 2. [MF0223_3_EXPR_02_Alexander_Daniela](MF0223_3_EXPR_02_Alexander_Daniela/)
#### Ejercicio 2: Historial de comandos en Linux

En este ejercicio, se documentó el uso de comandos de Linux para configurar un entorno de desarrollo. Las tareas realizadas incluyen:

- Instalación de herramientas (`nano`, `tree`).
- Creación de una estructura de carpetas para un proyecto de desarrollo.
- Creación de archivos básicos como `index.html`, `App.js`, `main.css`, entre otros.
- Uso de comandos como `chmod`, `cp`, `mv`, y `rm` para gestionar permisos, copias, y movimientos de archivos.
- Uso del comando `tree` para visualizar la estructura del proyecto.

Archivo relevante:
- [ejercicio2.md](MF0223_3_EXPR_02_Alexander_Daniela/ejercicio2.md)

---

### 3. [MF0223_3_EXPR_03_Alexander_Daniela](MF0223_3_EXPR_03_Alexander_Daniela/)
#### Ejercicio 3: Identificación y solución de problemas de consumo de recursos

En este ejercicio, se analizaron y resolvieron problemas relacionados con el consumo excesivo de CPU, memoria y disco en un sistema Linux. Las soluciones implementadas incluyen:

- **CPU:** Identificación y eliminación de procesos que consumen el 100% de la CPU, como el comando `yes > /dev/null`.
- **Memoria:** Eliminación de archivos temporales generados que saturaban la RAM y el swap.
- **Disco:** Eliminación de archivos generados por un script que saturaba el espacio en disco.

Se utilizaron herramientas como `top`, `ps aux`, `free -h`, y `df -h` para monitorear el sistema, y comandos como `kill` y `rm` para solucionar los problemas.

Archivo relevante:
- [ejercicio3.md](MF0223_3_EXPR_03_Alexander_Daniela/ejercicio3.md)

---

## Cómo usar este repositorio

1. **Ejercicio 1:** Para probar la configuración de Docker Compose, navega a la carpeta `MF0223_3_EP_01_Alexander_Daniela` y ejecuta:
   ```bash
   docker-compose up


# COMO SUBÍ EL PROYECTO PARA GITHUB

## 1. He creado un repositorio en GitHub
- Ingresé a mi cuenta de GitHub.
- Hice clic en el botón "New" para crear un nuevo repositorio.
- Le asigné un nombre al repositorio.
- He seleccionado la opción de visibilidad (público o privado).
- Luego hice clic en "Create repository".
- Copié la URL del repositorio recién creado.
- He abierto una terminal en mi ordenador y navegué hasta el directorio del proyecto.
- Inicialicé un repositorio Git local con el comando `git init`.
- Agregué los archivos del proyecto al área de preparación con `git add .`.
- Realizé un commit con un mensaje descriptivo usando `git commit -m "Mensaje del commit"`.
- He vinculado el repositorio local con el remoto en GitHub utilizando `git remote add origin <URL del repositorio>`.
- Subí los cambios al repositorio remoto con `git push -u origin master` (o `main` si nuestra rama principal se llama así).



