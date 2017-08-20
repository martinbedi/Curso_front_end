# Curso Front End

## Herramientas Básicas

* Git es un software de control de versiones
	* GitHub: [https://github.com/](https://github.com/)
	* Git para Windows: [https://git-for-windows.github.io/](https://git-for-windows.github.io/)
* SublimeText es un editor de texto para programar, escribir archivos Markdown y prosa: 
	* [https://www.sublimetext.com/](https://www.sublimetext.com/)
* Google Chrome es un navegador web.
	* [https://www.google.es/chrome/browser/desktop/index.html](https://www.google.es/chrome/browser/desktop/index.html)

## Git

Al iniciar un proyecto lo primero que se debe hacer es crear un repositorio en
Github. Despues de creado, creamos una carpeta en local que contendrá nuestro 
proyecto. Debemos acostumbrarnos a usar consola con el programa Git Bash en 
windows o en consola para macOS y Linux.

1) Debemos entrar en la carpeta del proyecto usando el comando `cd`. Por ejemplo,
si la carpeta está en el escritorio y se llama `carpeta`, entonces ejecutamos
`cd Desktop/carpeta`. Recordando siempre que al presionar `tab` nos autocompleta
las rutas de las carpetas y archivos.
2) Una vez dentro usamos `git init` para decirle al sistema que vamos a usar esa
carpeta como un repositorio git local.
3) Creamos un archivo README.md con el titulo del proyecto precedido de un # y 
lo guardamos en la carpeta del proyecto. Por ejemplo, si el proyecto es `Google`
escribimos en el archivo algo como `# Google`. Este archivo sirve como 
documentación de lo que es el proyecto y como debe utilizarse.
4) En este momento ya podemos mirar el estatus del proyecto en Git Bash. Usamos
`git status`para mirar que archivos fueron eliminados, agregados o modificados
desde la versión anterior del proyecto. Como apenas estamos comenzando, el archivo
README.md debe aparecer como nuevo.
5) Para almacenar el nuevo archivo README.md a una nueva version del proyecto
debemos usar `git add README.md`
6) Para crear la nueva version del proyecto en local con los cambios usamos
`git commit -m "primer commit"`
7) Hasta este punto tenemos almacenada una primera versión de nuestro proyecto
en local. Sin embargo, es posible que queramos usar un almacenamiento en la nube
y para eso está GitHub. Tomamos la URL del proyecto en GitHub (comienza en 
`git://` y termina en `.git`) y ejecutamos el siguiente comando `git remote add
origin [ulr del proyecto]` y esto hace que tengamos un alias para el servidor 
remoto del repositorio en GitHub. Por ejemplo, `git remote add origin git://github.com/martinbedi/Curso_front_end.git`.
8) En este momento, si nunca has trabajado con Git debes informarle a GitHub tu
nombre de usuario y contraseña usando los comandos 
`git config --global user.name "martinbedi"` y 
`git config --global user.email "martinbedi@hotmail.com"`
9) Para enviar los cambios locales (despues de hacer commit) al servidor usamos
`git push origin master`.

Apartir de este momento ya estamos listos para trabajar con Git y GitHub, entonces
cada vez que hagamos un cambio en el proyecto debemos almacenarlo en el 
repositorio local y en el de la nube (GitHub).

1) `git status` para ver que cambio de la versión pasada a la de ahora.
2) `git add [nombre del archivo o carpeta]`. Este comando se debe aplicar solo
a los archivos que queramos agregar a una nueva versión del proyecto.
3) `git commit -m "mensaje"`. Se almacena una nueva versión del proyecto en el
repositorio local. El mensaje debe ser algo explicativo de lo que 
cambio de la versión anterior a la de ahora.
4) `git push origin master`. Guardamos la nueva versión en la nube.

Sin embargo, hay momento en los que no solo somos nosotros los que trabajamos en
el proyecto, sino que hay más personas, por lo que siempre debemos estar pendientes
de los cambios en el repositorio en la nube para actualizar en nuestro. Por eso,
antes de ejecutar los comando explicados encima debemos ejecutar:

1) `git fetch`. Esto trae la versión más reciente de la nube para el local.
2) `git rebase origin/master`. Esto  mezcla nuestros cambios con la versión
más reciente del proyecto en el servidor en la nube.
