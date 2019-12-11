# CyanogenMod

+ Proyecto open-source obsoleto (por LineageOS). Es un sistema operativo para moviles , de codigo abierto y software libre, basado en las releases oficiales de android de google.
+ En 2015 habia unas 50 millones de personas usando CyanogenMod.
+ Era tambien usado como punto de partida para otras ROM.

+ En 2013, se constituyo como empresa para poder comercializarlse. Pero el jefe de aquel entonces no quería obtener beneficios económicos y por tanto en 2016 se fue. 
+ Mientras que el codigo fue open source, se hicieron forks y el desarrollo continuó por el lado de LineageOS.

> CyanogenMod was also said to increase performance and reliability compared with other official firmware releases.

> LineageOs y el milagro de la eterna juventud: asi disfrutan de Android 9.0 Pie smartphones de hace 5 años

https://www.xataka.com/moviles/lineageos-milagro-eterna-juventud-asi-disfrutan-android-9-0-pie-smartphones-hace-5-anos

# Breve historia de su nacimiento:

+ En 2008, tras el lanzamiento del HTC Dream, se descubrio que se podia ganar privilegio "root" en android. Con esto, y la naturaleza open-source del proyecto, se podia modificar el firmware de stock y reinstalarlo de nuevo.

+ Google "fixeo el bug"

+ En 2009 se dio a conocer CyanogenMod, que era una ROM que habia comenzado un desarrollador de software de Samsung. 

+ Se empezo a contribuir y a sacar soporte para distintos modelos de moviles.
+ Estaba en github y se contribuia mediante Gerrit. Las contribuciones se probaban, votaban y aceptaban. 

+ XDA Developers

+ Locked bootloaders

# AOSP contributing

+ https://source.android.com/setup/contribute
## Contribute to the code:
> Code is king , we'd love to review any changes that you submit, so check out hte source , pick a bug or a feature and get coding. The smaller and more targeted your patch submissions, the easier it is for us to review them

## Life of a patch:
![life of a patch](https://source.android.com/images/workflow-0.png)

## Life of a patch(en resumen):

1. Preparar el entorno en local (Git y repo)
2. Pull del repo
3. Desarrollo en local
4. Submit del commit de un Gerrit review. 
5. Se prueba el parche.
5.1 Si no funciona:
> verifier usets _code looks good_ bit, añade comentarios y notifica al autor.
5.2 Si funciona:
> Verifier sets _verified bit_ , acepta el cambio y lo commitea

## Para desarrollar, necesitas:
1. Git: control de versiones 
2. Repo: Programa de google que corre encima de Git.

https://source.android.com/setup/contribute/submit-patches
