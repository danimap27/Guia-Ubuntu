# Guía de Instalación de Dual Boot Windows y Ubuntu
Guia para instalar dual boot Windows y Ubuntu. Personalizar ubuntu para rendimiento de desarrollador.
## Requisitos del Sistema
Asegúrate de que tu sistema cumple con los siguientes requisitos antes de comenzar la instalación:
- **Sistema Operativo:** [Windows](https://www.mediafire.com/file/i026wqg4coyqw59/Windows+10+LTSC+2021.iso/file) y [Ubuntu](https://ubuntu.com/download/desktop).
- **Espacio en Disco:** Partición libre para Ubuntu (Recomendado minimo 10GB).
- **Memoria RAM:** Si en tu ordenador funciona Windows correctamente no tendras problema al instalar Ubuntu.
## Preparacíon de Windows
1. **Acceder a administracion de discos (Particiones):**

   <p align="center">
      <img src="https://github.com/danimap27/Guia-Ubuntu/assets/74870961/7ca07fc5-6776-4b46-acd6-a561f95946c3">
   </p>
   
3. **Pulsamos click derecho a la partición donde queramos instalar ubuntu (También se podria usar otro disco duro a parte):**
   
   <p align="center">
      <img src="https://github.com/danimap27/Guia-Ubuntu/assets/74870961/f5aed04e-231c-40f1-9783-d8d49d313c67" width="400" height="300">
   </p>
   
4. **Una vez hayamos decidido la cantidad de memoria de disco que vayamos a asignar a Ubuntu le damos a reducir y nos aparecera una particion en el disco donde se puede observar la memoria asignada:**

   <p align="center">
      <img src="https://github.com/danimap27/Guia-Ubuntu/assets/74870961/9f3857af-93ce-4f66-a35f-07da5519c2ff">
   </p> 

## Instalación de Ubuntu

1. **Descarga la Imagen de Ubuntu:**
   - Visita el sitio web oficial de [Ubuntu](https://ubuntu.com/download/desktop) y descarga la última versión estable.

2. **Crear un USB de Arranque:**
   - Utiliza herramientas como [Rufus](https://rufus.ie/es/) o [Balena](https://etcher.balena.io/#download-etcher) (en Windows) o dd (en Linux) para crear un USB de arranque con la imagen de Ubuntu.
   - En la herramienta que hayamos descargado seleccionamos el dispositivo que queramos utilizar como USB de arranque y seleccionamos el SO que queramos instalar.
     
   <p align="center">
      <img src="https://github.com/danimap27/Guia-Ubuntu/assets/74870961/80529f67-6fa8-4b2b-bff7-34dc7de73c7a" width="400" height="500">
   </p>

3. **Arranca desde el USB:**
   - Reinicia tu ordenador y arranca desde el USB.
   
     <img src="https://github.com/danimap27/Guia-Ubuntu/assets/74870961/2ff9b906-9b38-4786-a051-828b74cb9db6">
   

4. **Instalación de Ubuntu:**
   - Sigue el asistente de instalación.

     <img src="https://github.com/danimap27/Guia-Ubuntu/assets/74870961/7c105327-37ec-4b82-a152-10273b849fbe" width="85%" height="85%">

     <img src="https://github.com/danimap27/Guia-Ubuntu/assets/74870961/1b5134b1-5f33-42d6-ba09-e5a97c17b02e" width="85%" height="85%">

   - Selecciona la opción de instalación junto a Windows (dual boot).
     
      <img src="https://github.com/danimap27/Guia-Ubuntu/assets/74870961/377c549d-fb6e-4384-8727-82f37313e5b8" width="85%" height="85%">
   
4. **Instala el Cargador de Arranque (GRUB Customizer):**
   - Instalar GRUB Customizer.
     
     ```bash
     sudo apt install grub-customizer
     ```
   - Completa la instalación y reinicia.
     
4. **Personalizar GRUB de forma manual:**
   - Edita el archivo `/etc/default/grub` para ajustar las configuraciones, como el tiempo de espera, el fondo de pantalla, etc.
   - Después de editar, ejecuta `sudo update-grub` para aplicar los cambios.
   - Si prefieres que Windows sea la opción predeterminada en GRUB, puedes ajustar la prioridad de arranque en el archivo `/etc/default/grub`.
     
# Personalización de Ubuntu

## Comandos Básicos en Bash

### Navegación y Manipulación de Archivos/Directorios

- `ls`: Listar archivos y directorios.
- `cd`: Cambiar de directorio.
- `pwd`: Mostrar el directorio actual.
- `mkdir`: Crear un nuevo directorio.
- `cp`: Copiar archivos/directorios.
- `mv`: Mover o renombrar archivos/directorios.
- `rm`: Eliminar archivos/directorios.
- `touch`: Crear un archivo vacío.

### Visualización de Contenido

- `cat`: Mostrar el contenido completo de un archivo.
- `more` / `less`: Visualizar contenido paginado de un archivo.
- `head`: Mostrar las primeras líneas de un archivo.
- `tail`: Mostrar las últimas líneas de un archivo.

### Edición de Archivos de Texto

- `nano` / `vim` / `emacs`: Editores de texto en la terminal.

### Trabajo con Archivos Comprimidos

- `tar`: Comprimir o descomprimir archivos en formato tar.
- `zip` / `unzip`: Comprimir o descomprimir archivos en formato zip.

### Redirección y Pipes

- `>`: Redirigir la salida estándar a un archivo (crear o sobrescribir).
- `>>`: Redirigir la salida estándar a un archivo (agregar al final).
- `<`: Redirigir la entrada estándar desde un archivo.
- `|`: Pipe, redirige la salida de un comando como entrada a otro.

### Permisos y Propietarios

- `chmod`: Cambiar permisos de archivos/directorios.
- `chown`: Cambiar el propietario de archivos/directorios.
- `chgrp`: Cambiar el grupo de archivos/directorios.

### Procesos y Tareas

- `ps`: Mostrar información sobre procesos en ejecución.
- `kill`: Terminar un proceso.
- `bg` / `fg`: Poner un proceso en segundo/plano o primer plano.
- `jobs`: Mostrar trabajos en segundo plano.

### Variables de Entorno

- `export`: Establecer variables de entorno.
- `echo $VARIABLE`: Mostrar el valor de una variable de entorno.

### Ayuda y Documentación

- `man`: Mostrar el manual de un comando.
- `--help`: Obtener ayuda para un comando específico.

### Otros Comandos Útiles

- `grep`: Buscar patrones en archivos o salida de comandos.
- `find`: Buscar archivos y directorios en el sistema.
- `ssh`: Conectar a un servidor remoto de forma segura.

## Personalizacion de terminal de Ubuntu
La persolizacion de la terminal la vamos a hacer con [ohmybash](https://github.com/ohmybash/oh-my-bash)

¡Disfruta de tu sistema dual boot personalizado!
