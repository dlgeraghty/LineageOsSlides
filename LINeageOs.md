---
title:
- Lineage Os LIN 2019
author:
- David Lopez, Andres Cardenal 
theme:
- Copenhagen
---

[//]: <> (https://forum.xda-developers.com/chef-central/android/guide-android-rom-development-t2814763)
# LineageOs

![LineageOs logo](lineage.png)\ 

# Indice

1. Introduccion
2. Contribuir a LineageOS
3. Instalar LineageOS

# Introduccion

1. Contexto
2. Historia
3. Curiosidades
4. Referencias

# Contexto
1. LineageOs
2. Software libre
	
# LineageOS

## Qué es LineageOs?

LineageOs es sistema operativo que se trata de un fork de
Android, por tanto, es software libre y está orientado a su
uso en teléfonos inteligentes y tabletas.

# Que es el software libre? 

##  100 Libertades del software libre

+ 001 - Usar
+ 010 - Estudiar
+ 011 - Compartir
+ 100 - Mejorar 

# Fork 

## Qué es un Fork?

Fork en castellano, bifurcación, se trata de una distribución
no oficial de un proyecto de software. La bifurcación se
asienta sobre el código original ampliándolo o modificándolo
significativamente.

# Historia

Todo empezó con...

+ CyanogenMod
+ Fork a Lineage

# CyanogenMod

## CyanogenMod

+ HTC Dream
	- Se logra escalar privilegios (root)
+ Ventajas sobre el Android convencional
	- *El elixir de la eterna juventud*
+ Popularizacion
	- 50 millones de instalaciones en 2013...
+ Versiones de CyanogenMod 
	- Cyanogenmod 3 - 14.1 (Android 1.5 hasta 7.1.x)
+ Comercializacion
	- El inicio del fin
+ Fork a Lineage

# Ventajas frente a Android

## Herramientas que ofrecia no incluidas en Android

+ Soporte nativo de temas
+ Privacy Guard
+ Tethering mediante Wi-Fi , Bluetooth o USB

## Mejora en la calidad del software

+ Mejoraba el rendimiento
+ Mejora la fiabilidad
+ Combate el spyware y el bloatware

# Controversias

## Discusion con Google 

+ En Septiembre de 2009 , Google envio una carta de cese  
y desistimiento a Cyanogen debido a que en CyanogenMod  
se incluian aplicaciones de software privativo de Google

## Violacion de la provacidad

+ En Abril de 2013, los desarrolladores de CyanogenMod,  
Decidieron deshabilitar la opcion de estadisticas siendo  
posteriormente otra vez habilitada


# Contribuir a LineageOs

+ To contribute, you'll need to be able to produce builds for your device. Pick your device from our list of supported devices to get started.
+ Once you’re successfully running your own build, you can begin to make your changes.
+ Once you’ve finished making your change, simply follow our guide on submitting to Gerrit.

# Contribuir a LineageOs(1)

Nos encontramos con varios problemas:

+ Como se produce una compilacion (build) para mi dispositivo
+ Y si no esta entre los oficiales...? (Mal asunto)

# Contribuir a LineageOs(2)

## Como compilar una version de LineageOs? (preparacion)
+ 1x Ordenador de la NASA (con linux)
+ Adb y fastboot
+ Estos pocos paquetes:
bc bison build-essential curl flex g++-multilib gcc-multilib git gnupg gperf lib32ncurses5-dev lib32readline-gplv2-dev lib32z1-dev libesd0-dev
liblz4-tool libncurses5-dev libsdl1.2-dev libwxgtk2.8-dev libxml2 libxml2-utils lzop pngcrush schedtool squashfs-tools xsltproc zip zlib1g-dev
imagemagick
+ Java
+ Repo

# Contribuir a LineageOs(3)

## Como compilar una version de LineageOs? (inicializar codigo)
+ Inicializar el repositorio:  
repo init -u https://github.com/LineageOS/android.git -b cm-13.0  
+ Descargar el codigo:  
repo sync  
Note: This may take a while, depending on your internet speed. Go and have a beer/coffee/tea/nap in the meantime!

# Contribuir a LineageOs(4)

## Como compilar una version de LineageOs? 
+ Obtener las aplicaciones por defecto:  
cd /vendor/cm  
./get-prebuilts
+ Preparar el codigo especifico paranuestro dispositivo:  
source build/envsetup.sh  
breakfast manta
+ Extraer el codigo propietario:  
./extract-files.sh

# Contribuir a LineageOs(5)

## Como compilar una version de LineageOs? (por fin)

+ activar el mecanismo de cache:  
export USE_CCHACHE=1
+ especificar la cantidad de disco que queremos usar para cache:  
prebuilts/misc/linux-x86/ccache/ccache -M 50G
+ Start the build:  
croot  
brunch manta  
+ Install the build:  
cd $OUT
+ Esto produce un recovery.img

# Contribuir a LineageOs(6)

## Entonces...facil...no?
+ Quien escribio este comentario en el tutorial no diria lo mismo:  
The key point here is that you say run the extract-files.sh script. However, if your device is not supported it doesn't tell you how to update the script to list the files that need extracting for your device.
+ En respuesta al anterior:  
Thanks man, you saved me a lot of vain effort. The title is misleading.

# Contribuir a LineageOs(7)
+ Entonces como obtenemos LineageOs para un dispositivo que no esta en la lista oficial?

## Buscando en muchos foros, la mejor respuesta:
Porting Android to a new device is a hard task and there is no single manual for it.  

I suggest you go to https://source.android.com/ and read everything about Android builds.  

Basically, you need those things:  

1. A device tree

2. The kernel

3. Vendor blobs

[//]: <> (https://www.lineageosrom.com/2017/01/how-to-build-lineageos-rom-for-any.html)

# Contribuir a LineageOs(Gerrit)

*Gerrit es un servidor y administrador de repositorios git.*

[Gerrit de LineageOs](https://review.lineageos.org/q/status:open)

## Guia para enviar un parche:
[documentacion oficial](https://wiki.lineageos.org/submitting-patch-howto.html) 

1. Setup
	+ Configurar git y ssh
	+ Preparar directorios de trabajo
2. Enviar a Gerrit
	+ Subir cambios
3. Revision de tu envio

# Gerrit (subir cambios)

## Empezar una nueva rama
+ repo start \<branch name\> \<project name\>

## Aplicar cambios en git (local)
+ git add .  
+ git commit ...

## Subir los cambios a Gerrit:
+ repo upload .

# Revision de cambios:

## Incorporar revisores
+ Que sean mantenedores de tu dispositivo

## Etiquetar el parche segun el estado
+ No fusionar, preferiria que no se fusionase  
, a mi me parece que esta bien pero necesita  
revision, a mi me parece bien , aprobado! 

# Instalacion 

+ *Puedes intentarlo, siempre que no tengas un iphone...*


Como instalar

1. Requisitos 
2. Instalacion

# (Pre)Requisitos

*Sin esto...no vamos bien...*

1. Bootloader desbloqueado
	+ Gestor de arranque
	+ [articulo sobre bootloader](https://www.andro4all.com/2019/01/bootloader-android-desbloquear)	
2. Custom recovery instalada
	+  Particion de arranque independiente del sistema
	+ [articulo sobre recovery](https://www.xatakandroid.com/tutoriales/como-entrar-al-modo-recovery-en-android) 

# Besbloquear bootloader

*O cambiarte de movil en el intento*

## Metodo: Fastboot & ADB
	Atencion, esto hara reset de fabrica y   
		violara la garantia
	1. Obtener ADB y fastboot
	2. Habilitar opciones de desarrollador
	2.1 Habilitar USB debugging
	2.2 Habilitar desbloqueo OEM
	3. Conectar el telefono por usb y   
		permitir el USB debugging
	4. (Paso critico) adb reboot bootloader 
	5. fastboot flashing/oem unlock
	6. fastboot reboot
# Bootloader

## El bootloader es algo como:
![Android bootloader](bootloader.jpeg)

# Custom Recovery (TWRP)

+ *Importante, descargar el twrp valido para tu movil,  
	si no, experimentar...*

## Metodo: ADB y Fastboot
	1. Adb reboot bootloader
	2. fastboot flash recovery archivo_con_tu_twrp
	3. fastboot reboot

## Metodo 2: TWRP Manager (app)
	Mas sencillo que la anterior, si tu movil  
	es compatible...
	1. Descargar la app y seguir los pasos...

<https://www.xda-developers.com/how-to-install-twrp/ >

# TWRP

## TWRP se parece a:
![TWRP image](twrp.png)

# Instalacion!

1. Obtener la ROM...facil...no?
2. Gapps? Huimos de google para volver a el?
3. Instalar

# Obtener la ROM

1. Oficial de LineageOs
2. Foro de XDA Developers

# Oficial de LineageOs

![list of officially supported devices by LineageOs](devices1.png)
![list of officially supported devices by LineageOs](devices2.png)

# Foro de XDA Developers

![xda developers forum](xda.png)

# Instalar (como yo lo hago)

* Guardar la ROM en una sd externa
* Insertar la SD y bootear a twrp
* (Backup?)
* Wipe
* Install: seleccionar la ROM (y las GAPPS)

# Video de apoyo:

[![install lineage os](video.png)](https://www.youtube.com/watch?v=5snxtA5e2RY "install lineage os")
