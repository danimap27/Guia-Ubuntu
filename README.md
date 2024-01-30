# Guía de Instalación de Dual Boot Windows y Ubuntu
Guia para instalar un doble boot Windows y Ubuntu. Personalizar ubuntu para rendimiento de desarrollador
## Requisitos del Sistema

Asegúrate de que tu sistema cumple con los siguientes requisitos antes de comenzar la instalación:

- **Sistema Operativo:** Windows y Ubuntu.
- **Espacio en Disco:** Partición libre para Ubuntu.
- **Memoria RAM:** Requisitos mínimos para ambas plataformas.
## Preparacíon de Windows
1. **Acceder a administracion de discos (Particiones)**
   
   ![image](https://github.com/danimap27/Guia-Ubuntu/assets/74870961/f3e1badb-949c-4205-8fa3-0b3746f5991d)
   
2. **Pulsamos click derecho a la partición donde queramos instalar ubuntu (También se podria usar otro disco duro a parte)**
   
   ![image](https://github.com/danimap27/Guia-Ubuntu/assets/74870961/f5aed04e-231c-40f1-9783-d8d49d313c67)
   
3. **Una vez hayamos decidido la cantidad de memoria de disco que vayamos a asignar a Ubuntu le damos a reducir y nos aparecera una particion en el disco donde se puede observar la memoria asignada**

   ![image](https://github.com/danimap27/Guia-Ubuntu/assets/74870961/9f3857af-93ce-4f66-a35f-07da5519c2ff)

## Instalación de Ubuntu

1. **Descarga la Imagen de Ubuntu:**
   - Visita el sitio web oficial de Ubuntu y descarga la última versión estable.

2. **Crear un USB de Arranque:**
   - Utiliza herramientas como Rufus (en Windows) o dd (en Linux) para crear un USB de arranque con la imagen de Ubuntu.

3. **Arranca desde el USB:**
   - Reinicia tu computadora y arranca desde el USB.

4. **Instalación de Ubuntu:**
   - Sigue el asistente de instalación.
   - Selecciona la opción de instalación junto a Windows (dual boot).
   - Configura la partición para Ubuntu.

5. **Instala el Cargador de Arranque (GRUB):**
   - Instala el GRUB en la misma partición que Ubuntu.
   - Completa la instalación y reinicia.

## Configuración Post-Instalación

1. **Personalizar GRUB:**
   - Edita el archivo `/etc/default/grub` para ajustar las configuraciones, como el tiempo de espera, el fondo de pantalla, etc.
   - Después de editar, ejecuta `sudo update-grub` para aplicar los cambios.

2. **Configurar la Prioridad de Arranque (si es necesario):**
   - Si prefieres que Windows sea la opción predeterminada en GRUB, puedes ajustar la prioridad de arranque en el archivo `/etc/default/grub`.

## Personalización Adicional de Ubuntu

1. **Temas y Fondos de Pantalla:**
   - Explora la Configuración de Apariencia para cambiar temas y fondos de pantalla.

2. **Scripts de Inicio:**
   - Agrega tus propios scripts de inicio en `~/.config/autostart` para ejecutar aplicaciones al inicio.

3. **Personalizar el Bash Prompt:**
   - Modifica el archivo `~/.bashrc` para personalizar tu prompt de bash.

4. **Instalar y Configurar Aplicaciones:**
   - Utiliza el administrador de paquetes `apt` para instalar nuevas aplicaciones.
   - Configura aplicaciones según tus preferencias.

5. **Optimizar el Rendimiento (opcional):**
   - Instala controladores gráficos y otros controladores específicos para mejorar el rendimiento.

Recuerda consultar la documentación oficial de Ubuntu y GRUB para obtener información adicional y solucionar problemas comunes. ¡Disfruta de tu sistema dual boot personalizado!
