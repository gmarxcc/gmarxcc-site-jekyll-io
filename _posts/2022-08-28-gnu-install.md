---
layout: post
title: "Instalación de un sistema operativo GNU"
date: 2022-08-28
author: Gerardo Marx
categories: lecture engineering ai
---
![](https://tutorialesenlinea.es/uploads/posts/2019-10/1570382062_gnu-linux_tutoriales_en_linea.webp)

# Introducción al OS GNU

GNU es un entorno de trabajo que utiliza como núcleo principal el *Linux* desarrollado por Linus Torvalds; sin embargo, todo el sistema operativo que conocemos en la actualidad no es Linux. 

Este núcleo o *Kernel* es el encargado de administrar los recursos de la máquina usados por las diferentes aplicaciones que el sistema y el usuario utilizan. Entonces, el núcleo Linux es utilizado junto con otra serie de aplicaciones del proyecto GNU que crean el sistema operativo completo GNU. Dependiendo de las herramientas que se incluyan en el OS, se generan distribuciones diferente que abarcan las necesidades de usuarios diferente y se les denomina GNU/Linux; es decir sistema operativo GNU con el *Kernel* LinuX[^1].

El proyecto GNU se fundamenta en el Software Libre: libertad de los usuarios para ejecutar, copiar, distribuir, estudiar, modificar y mejorar el software. GNU es un OS tipo Unix[^2]; esto quiere decir que que el OS es una colección de muchos programas: aplicaciones, bibliotecas, herramientas de desarrollo y hasta juegos. 

GNU (se pronuncia *ñu* en español) es un acrónimo recursivo de *GNU No es Unix* y engloba un gran número de proyectos de software libre para cubrir una necesidad particular. Por ejemplo, Linus Torvalds escribió un kernel tipo Unix (Linux), Donald Knuth un editor de textos (TeX), Bob Scheifler un sistema de manejo de ventanas (X window system), entre muchos otros. Es importante indicar que el gran promotor y activista del movimiento del Software Libre para el sistema GNU es Richard Stallman quien aporto con importantes herramientas del sistema GNU como Emacs.

# Instalación dual de Ubuntu junto con Windows

Como comentamos anteriormente existen gran cantidad de distribuciones GNU. Sin embargo, una muy amigable con el usuario que está acostumbrado al entorno de Windows, es Ubuntu. Ubuntu actualmente ha lanzado la versión 21.04, pero yo personalmente te recomiendo empezar con la versión 18.04 *Bionic Beaver*. 

Más adelante te pondré el enlace a dos guías: una para instalar con Windows 10-7 y otra para windows 11; aunque son muy similares. Sin embargo, permíteme indicarte de manera general el procedimiento y los cuidados que debes de tener con tu sistema. 

De manera general lo recomendable es: 
1. Hacer una copia de seguridad de archivos muy importantes o sincronizar tu nube con los datos.
2. Crear espacio en tu disco duro para instalar ubuntu, al menos unos 50GB.
3. Crear un USB de arranque con Ubuntu
4. Instalar Ubuntu 18.04
5. Reiniciar el equipo para verificar el *Dual Boot*.


Las ligas de los tutoriales que te dejo a continuación incluyen detalles, imágenes y en algunos caos también vídeos. No obstante el procedimiento también es descrito aquí con algunas variantes que pueden ayudar a mejorar la experiencia. 

Ligas: 
- [Como instalar ubuntu junto con windows](https://tecnoespectro.com/como-instalar-ubuntu-junto-con-windows-configuracion-de-arranque-dual/)
- [How to install Ubuntu 20.04 and dual boot alongside Windows 10](https://medium.com/linuxforeveryone/how-to-install-ubuntu-20-04-and-dual-boot-alongside-windows-10-323a85271a73)

# Procedimiento

## Paso 1: Hacer copia de seguridad

Mi recomendación general para este paso es crear una cuenta en Google y aprovechar la aplicación *Drive* para migrar la información más importante al nuevo sistema que usarás más frecuentemente, incluso si planeas seguir usando ambos OS (windows y ubuntu), puedes sincronizar información usando este medio y evitar accesar a la otra partición, por aquello del *malwere* siempre presente en Windows.

Otra opción es usar alguna herramienta de sincronización de archivos entre tu máquina y un disco duro externo, sinceramente no conozco herramienta en Windows pero normalmente viene una con el disco duro que compraste.

## Paso 2: Crear una partición en tu disco duro

Si tienes otro disco duro puedes usarlo para instalar la distribución ubuntu, **pero todo lo que está en ese disco se perderá durante la instalación**.

Sino tienes otro disco duro que puedas usar lo recomendable es **crear una partición para probar el sistema GNU**. Para eso es necesario reducir el espacio que usa Windows utilizando la aplicación `diskmgmt.msc` en Windows. 

Para acceder a la aplicación presiona las teclas `Windows+R` y aparecerá la aplicación `Run` que permite ejecutar aplicaciones con solo saber su nombre. Por lo tanto escribe en la ventana `diskmgmt.msc` y presiona `OK`.

Esto abrirá la administración de las particiones en Windows. En la ventana principal aparecerán todos los discos duros de tu máquina; recuerda que en Windows un disco puede tener varias particiones que en el administrador aparecerán como volúmenes diferentes (C:, E:, E:, etc).

Ahora haz click derecho en la partición del disco que quieras reducir para instalar Ubuntu, selecciona la opción *shrink*.

En la única casilla que te permite cambiar, *enter the amount of space to shrink in MB*, ingresa el valor en MB que quieras librar para Ubuntu; mi recomendación es 100,000 MB o mínimo 50,000 MB. Y finalmente haz click en `Shrink`.

Después de unos minutos se creará la partición deseada y podrás visualizarla en el administrador.

## Paso 3: Crear un USB-Live

Descarga el archivo ISO de ubuntu 18.04 en este link o busca el archivo en la página de Ubuntu, versión Desktop.

Para crear una versión *Booteable* de ubuntu descarga cualquiera de las siguiente aplicaciones: Universal USB Installer o Ballena Etcher. Con cualquiera de las herramientas, siga las instrucciones de la aplicación para  montar el ISO descargado de Ubuntu en una USB con mínimo 8GB.

## Paso 4: Instalación de Ubuntu
Después de crear la USB de arranque, conéctelo a su máquina y reiníciela. Mientras el equipo enciende, presione la tecla que permite seleccionar el medio de arranque en modelos con UEFI, o configure el orden de inicio de arranque en un sistema basado en BIOS.

Una vez que inicies desde la USB, tienes la opción de probar o de instalar Ubuntu. Selecciona instalar Ubuntu y presiona `Enter`.

![](https://i0.wp.com/tecnoespectro.com/wp-content/uploads/Install-Ubuntu-Alongside-Windows-4.png?w=800&ssl=1)

Los siguientes pasos de la instalación se recomiendan de la siguiente manera:

1. Selecciona el idioma de tu teclado y del idioma deseado, seguramente español
2. En el tipo de instalción del sistema, mi recomendación es seleccionar **Minimal Installation**, así sólo se instalarán las aplicaciones básicas para empezar a trabajar con Ubuntu.
![](https://i0.wp.com/tecnoespectro.com/wp-content/uploads/Install-Ubuntu-Alongside-Windows-3.png?w=1024&ssl=1)
3. En la opción del **Boot manager**, selecciona **Install Ubuntu alongside Windows Boot Manager**, aparecerá una advertencia de cambios en el disco duro, da click en aceptar
![](https://i0.wp.com/tecnoespectro.com/wp-content/uploads/Install-Ubuntu-Alongside-Windows-1.png?w=1024&ssl=1)
4. Despues selecciona tu zona horaria y crea un usuario, así como su password
5. El proceso de instalación tomará un tiempo


## Paso 5: Reinicia el equipo

Una vez que la instalación ha terminado aparecerá un mensaje para reiniciar el equipo, antes de presionar el botón, primero retira el medio de instalación y de click en *restart now*. Una vez que el sistema se reinicie, pruebe entrar en ambos OS para verificar el arranque.

----


Hasta aquí este pequeña guía, espero pronto poder hacer un vídeo con el procedimiento para dejar aún más claro el proceso completo, aunque creo que esta guía es suficiente por el momento. Cualquier duda o comentario hazme lo saber por mis redes sociales que están abajo.


[^1]: https://www.gnu.org/gnu/linux-and-gnu.es.html
[^2]: https://www.gnu.org/home.es.html

