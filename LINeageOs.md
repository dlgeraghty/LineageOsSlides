---
title:
- LineageOs
author:
- David Lopez
theme:
- Copenhagen
---

# LineageOs

https://www.youtube.com/watch?v=5snxtA5e2RY

![LineageOs logo](lineage.png)

# Introduccion

Algo de introduccion

+ Punto 1
+ Punto 2
+ Punto 3

# Instalacion 

+ *Puedes intentarlo, siempre que no tengas un iphone...*


Como instalar

1. Requisitos 
2. Instalacion

# (Pre)Requisitos

*Sin esto...no vamos bien...*

1. Bootloader desbloqueado
2. Custom recovery instalada 

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
	4. (Paso critico) ``` adb reboot bootloader ```
	5. ```fastboot flashing/oem unlock```
	6. ```fastboot reboot```

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

https://www.xda-developers.com/how-to-install-twrp/ 


# Instalacion!

1. Obtener la ROM...facil...no?
2. Gapps? Huimos de google para volver a el?
3. Instalar

# Obtener la ROM

1. Oficial de LineageOs
2. Foro de XDA Developers

# Oficial de LineageOs

## oficial de LineageOs (recomendado)
![list of officially supported devices by LineageOs](devices1.png)
![list of officially supported devices by LineageOs](devices2.png)

# Foro de XDA Developers

## Foro de XDA Developers
![xda developers forum](xda.png)

# Instalar (como yo lo hago)

* Guardar la ROM en una sd externa
* Insertar la SD y bootear a twrp
* (Backup?)
* Wipe
* Install: seleccionar la ROM (y las GAPPS)
