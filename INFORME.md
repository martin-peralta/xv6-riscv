# Informe de Instalación xv6 - Tarea 0
# Grupo L


## En este informe se explica el paso a paso seguido para Instalar xv6 (Windows 11)


1.  **Preparación de GitHub**: Se hizo un fork del repositorio original de xv6-riscv en la cuenta de github @martin-peralta, para este caso y por comodidad de proyectos anteriores, se utilizó Github Desktop para clonar el repositorio y luego realizar una rama (la cual se colocó el nombre del alumno dueño del computador)
2.  **Instalación de WSL**: Se entró a cmd en Windows y verifique la instalación de WSL, la cual no exisita en el computador, por lo que ejecuté el siguiente comando:

* wsl --install

3.  **Instalación de Ubuntu**: Ya instalado WSL, al no tener una distribución de Linux en el computador, se instaló Ubuntu a través de cmd con el siguiente comando:

* wsl --install -d Ubuntu

4. **Habilitar Virtualización**: Durante la instalación de Ubuntu, apareció un error el cual solicitaba al usuario activar lo siguiente:

* Las caracteristicas de windows "Platadorma del hipervisor de windows" y "Subsitema de windows para Linux".
* Habilitar la virtualización en la BIOS del equipo.

Una vez realizado esto se pudo instalar correctamente Ubuntu.

4 **Instalación de Dependencias**: Se busco en la carpeta del repositorio creado (xv6-riscv) y dentro del archivo README se aclaraban las dependencias requeridas (toolchain de riscv y qemu), instalando todas las dependencias necesarias en la siguiente linea de comando: 

* sudo apt-get update && sudo apt-get install git build-essential gdb-multiarch qemu-system-misc gcc-riscv64-unknown-elf 

5 **Compilación y ejecución**: Ya con todo instalado, se ejecuta xv6 con el siguiente comando:

* make qemu

obteniendose la respeusta: "xv6 kernel is booting"

6 **Confirmación de funcionamiento**: Se confirma que xv6 funciona correctamente, el sistema compiló sin errores y se ejecutó en una ventana de qemu.
Además se pudieron ejecutar de manera correcta los siguientes comandos de prueba (los solicitados en el enunciado de la tarea):

* ls
* echo "Hola xv6"
* cat README

Lo cual esta documentado en la captura de pantalla adjunta a la entrega y al repositorio.
