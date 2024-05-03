
# Comandos Git

![App Screenshot](https://i.ibb.co/ch6Qt0p/GitHUB.png)



## Crear tu primer repositorio

- Ingresa a [![Github](http://img.shields.io/badge/-Github-000000?style=flat&logo=github&logoColor=FFFFFF)](https://github.com/)
- En el margen superior derecho hacer clic en **"Sign up"**, te dará la bienvenida, debes hacer clic debajo de **Enter your email**, ahí utilizá el correo con el que quieres compartir tu repositorio.

- Una vez ingresado tu correo hacer clic en **Conitnue**
- Luego te pedirá confirmar tu correo.
- Seguido a esto ingresar a https://github.com/dashboard, debes hacer clic en **New**, para crear un nuevo repositorio.
- Seguido de ello, debes proporcionar un *nombre para tu repositorio*, *una descripción opcional* y elige si el repositorio es **privado o público**.
- Puedes agregar un **README** sino sabes como crearlo, usa el sitio: https://readme.so/
- Seguido haz clic en **Create repository**.

## Video de un genio

[![Youtube](https://img.shields.io/badge/Youtube-ff0000?style=flat-square&logo=youtube&link=https://www.youtube.com/channel/UCn9XdNmBSqyIVlJLFm_7h1w?view_as=subscriber)](https://www.youtube.com/watch?v=1eEnboVooiY)


## Sign up

![App Screenshot](https://i.ibb.co/smf5bHF/Sing-up.png)


## Configuración inicial de Git

**Para realizar los siguientes pasos es necesario usar la terminal de windows/linux, pero también se puede usar git bash, puedes instalarlo usando el siguiente link: https://git-scm.com/downloads**

- Abrir Git bash o terminal (en windows puedes hacer con windows + R, escribir cmd y presionar enter) 👇

![App Screenshot](https://i.ibb.co/N7S4wJr/cmd.png)
- Configura tu nombre de **usuario** y **dirección de correo electrónico global** en Git y presionando **Enter** luego de escreibirlos, usá los siguientes comandos: 👇
1) 👉 **git config --global user.name "Tu Nombre"**
  ejemplo:
   git config --global user.name "Matias Giorgini"

  ```bash
  git config --global user.name
  ```

2) 👉 **git config --global user.email "tu@email.com"**

  ```bash
  git config --global user.email
  ```

  *Se recomienda usar el mismo correo con el que te registraste en github*

  - Crear un nuevo directorio (la carpeta donde realizarás el proyecto)
  - Windows: 

  👉 **botón derecho → Nuevo → Carpet** 
  
  (asignarle el nombre del proyecto)

  - Linux o terminal: 

👉 **mkdir mi-proyecto**

👉 **cd mi-proyecto**

## Inicializar un Repositorio Git Localmente

El comando para iniciar nuestro repositorio, o sea, indicarle a Git que queremos usar su sistema de control de versiones en nuestro proyecto

**Recuerda estar dentro de la carpeta del proyecto siempre para ejecutar los comandos**

*Ejemplo: C:/Documents/ProyectoNuevo*

👉 Ejecutar el comando: **git init**

```bash
git init
```

- Si no usas un ide (netbeans, intellijIdea, eclipse, visual studio code), puedes crear archivos usando el comando touch index.html por ejemplo.
  
- El comando para que nuestro repositorio sepa de la existencia de un archivo o sus últimos cambios: **git add .**
  ```bash
  git add .
  ```
- Para realizar el primer commit luego de hacer los cambios utiliza el comando: **git commit -m "Primer commit: Agregar archivos iniciales"**
  ```bash
  git commit -m ""
  ```
**Lo que se encuentra dentro de los "" es lo que tienes que modificar a gusto, recuerda ser lo más aclarativo posible, *por ejemplo* **"Primer commit: instalación de dependencias"**

- Conectar repositorio Local con el repositorio remoto

Ingresa al repositorio que creaste anteriormente, busca el **botón verde** de *<> Code* y puedes elegir dos opciones por **HTTPS o POR SSH**

![App Screenshot](https://i.ibb.co/q0kn0JR/repositorio-remoto.png)

Utiliza el siguiente comando para asociar el repositorio local con el remoto:

👉**git remote add origin url_del_repositorio_en_github>**

👉 Ejemplo: git remote add origin https://github.com/msgiorgini77/msgiorgini77.git

```bash
git remote add origin
```

**Recuerda presionar Enter al finalizar el comando**

- Crear una rama para trabajar usando el siguiente comando:

👉 **git checkout -b "NombreNuevaRama"**

```bash
git checkout -b
```

- Cambia de rama existente, usando el siguiente comando:

👉 **git checkout nombre-de-la-rama**

```bash
git checkout
```

- Si ya existen cambios subidos al repositorio debes utilizar el siguiente comando, para luego poder subir tus cambios con el comando push:

👉 **git pull origin main**

```bash
git pull origin
```

- Subir los cambios al repositorio remoto, utilizando una rama creada cuyo nombre es main, usamos el siguiente comando:

👉 **git push -u origin nombreDeLaRama**

```bash
git push -u origin
```

- Verificar el Estado del Repositorio, usamos el siguiente comando (ofrece una descripción del estado de los archivos (untracked, ready to commit, nothing to commit):

👉 **git status**

```bash
git status
```

- Si deseas eliminar archivos del index (. -r, filename) (–cached):

👉 **git rm**  

```bash
git rm
```

git rm no puede usarse por sí solo, así nomás. Se debe utilizar uno de los flags para indicar a Git cómo eliminar los archivos que ya no se necesitan en la última versión del proyecto:

git rm --cached : elimina los archivos del área de Staging y del próximo commit, pero los mantiene en nuestro disco duro.
```bash
git rm -- cached
```
git rm --force : elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos
recuperarlos si es necesario (pero debemos aplicar comandos más avanzados).

```bash
git rm --force
```

- Si deseas eliminar las ramas, tienes dos opciones, pero ten cuidado que se borran todas las líneas de código que hayas hecho:

## Eliminar una rama después de haber fusionado todos los cambios
👉 **git branch -d nombre_de_la_rama**

## Eliminar una rama incluso si tiene cambios sin fusionar
👉 **git branch -D nombre_de_la_rama**

3) Analizar cambios en los archivos de un proyecto Git:

git log: lista de manera descendente los commits realizados.
```bash
git log
```
git log --stat: además de listar los commits, muestra la cantidad de bytes añadidos y eliminados en cada uno de los archivos modificados.
```bash
git log --stat
```
git log --all --graph --decorate --oneline: muestra de manera comprimida toda la historia del repositorio de manera gráfica y embellecida.
```bash
git log --all --graph --decorate -- oneline
```
git show filename: permite ver la historia de los cambios en un archivo.
```bash
git show filename
```
git diff : compara diferencias entre en cambios confirmados.
```bash
git diff
```

**IMPORTANTE** Te puede salvar la vida ❤️

⚠️ **¿Como deshacer un commit en git?** ⚠️

Te dejo un link de Linkedin para que veas como hacerlo:

[![Linkeind](https://img.shields.io/badge/linkedin%20-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white 'LinkedIn Link')](https://www.linkedin.com/posts/midudev_tutorial-deshacer-commit-en-git-ugcPost-7164618355306360832-Wxod?utm_source=share&utm_medium=member_desktop)

- Te dejo otro comando que puede ser muy util:

👉 **git stash**

*El comando git stash en Git se utiliza para "apartar" temporalmente los cambios locales que no están listos para ser comprometidos (commited), permitiéndote trabajar en otra área del proyecto sin perder tus cambios actuales.*

⚠️ **¿Como volver en el timpo con branches y checkout** ⚠️

git reset --soft/hard: regresa al commit especificado, eliminando todos los cambios que se hicieron después de ese commit.
```bash
git reset --soft
```
```bash
git reset hard
```
git checkout : permite regresar al estado en el cual se realizó un commit o branch especificado, pero no elimina lo que está en el staging area.
```bash
git checkout
```
git checkout – : deshacer cambios en un archivo en estado modified (que ni fue agregado a staging)
```bash
git checkout -
```

## Algunos comandos más:

- **git add .**: Guarda todos los cambios realizados.
- **git show**: Muestra todos los cambios históricos hechos.
- **git stash save "mensaje"**: Aparta los cambios locales con un mensaje descriptivo.
- **git stash list**: Muestra la lista de apartados (stash) actual.
- **git stash apply**: Aplica el último cambio apartado al directorio de trabajo sin eliminarlo de la pila de apartados.
- **git stash pop**: Aplica el último cambio apartado y lo elimina de la pila de apartados.
- **git stash drop**: Elimina el último cambio apartado de la pila de apartados.


## Authors

- [Matias Giorgini](https://www.github.com/https://github.com/msgiorgini77)

|[![](https://img.shields.io/badge/github-%23121011.svg?&style=for-the-badge&logo=github&logoColor=white 'Github Link')](https://github.com/msgiorgini77) | [![](https://img.shields.io/badge/linkedin%20-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white 'LinkedIn Link')](https://www.linkedin.com/in/matias-giorgini/)
:------- | :-------

