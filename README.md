# clase-git-tel335

### Guia Cheat Sheet Git

[git-cheat-sheet-education.pdf
](https://education.github.com/)

### Instalacion de git

#### Windows

[Tutorial Windows 10 (No es de mi autoria, creditos correspondientes)](https://www.youtube.com/watch?v=WcYTcttEf50)

#### Linux

Debian / Ubuntu

```
sudo apt-get install git -y
```

#### Mac Os

[Tutorial Mac Os (No es de mi autoria, creditos correspondientes)](https://www.youtube.com/watch?v=CGhF_DzLqbE)


### Configurando Git

Debemos añadir nuestro nombre y apellido y correo a git mediante los siguientes comandos, cambiando Nombre Apellido" y "example@mail.com".

```
git config --global user.name "Nombre Apellido"
git config --global user.email "example@mail.com"
```

### Creamos las llaves SSH para configurar git

[Guia Oficial Generacion de llaves](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

Creando el par de llave SSH
```
ssh-keygen -t ed25519 -C "example@mail.com"
```

Se debe añadir la llave publica (.pub el contenido) en los ajustes de github

[Guia Para añadir la llave publica](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

Luego de generar las llaves hay que añadirlas en nuestro equipo al agente que es el que se encarga de guardar las llaves para usarlas automaticamente

```
ssh-add /ruta/par/de/llaves/ed25519
```

Comando utilizado para verificar que todo este bien
```
ssh -T git@github.com
```

### Comandos Mas utilizados

- Se utiliza para crear un rama y cambiarse a la misma (opcion -b la crea)

```
git checkout -b rama
```

- Se utiza para cambiarse de rama

```
git checkout -b rama
```

- Sirve para añadir al stage o decirle a git que indexe los archivos y carpetas, desde donde estoy posicionado mediante la terminal, tambien se utiliza para agregar los cambios de los archivos y carpetas.

```
git add .
```

- Sirve para al proceso que llevamos agregarle un mensaje que es un commit. Cada commmit que realizamos es un estado de avance. OJO: previamente hay que añadir los cambios mediante "git add .". 

```
git commit -m "mensaje descriptivo"
```

- Se utiliza para subir los cambios realizados en el commit  a la rama (desarrollo) del servidor remoto (Github) siempre va origin ya que origin significa que es nuestro equipo, lo que logramos es subir los cambios al servidor en la rama respectiva (desarrollo)

```
git push origin desarrollo
```

- Se utiliza para establecer por defecto la subida desde el origen a la rama de desarrollo

```
git push -u origin desarrollo
```

### Recordar  Realizar Pull Request desde su repositorio en su cuenta github a mi repositorio rama main (en el caso de los controles es hacia el repositorio del profesor Francisco la rama la dira el)

