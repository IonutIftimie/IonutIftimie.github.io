---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Proteger directorio"
categories: jekyll update
---

## 1. Crear directorio

Crear un directorio con el nombre de  `/protegido` y un indice.

![indice](/assets/img/indice.png)

<br>

## 2. Crear fichero de configuración

Creamos un fichero de configuración y lo activamos con `sudo a2enmod protegido.conf`

![protegido-conf](/assets/img/protegido-conf.png)

<br>

## 3. Crear usuario

Usando htpasswd añadimos usuarios y su contraseña



![usuarios](/assets/img/usuarios.png)



## 4. Comprobacion

Accedemos al sitio protegido e ingresamos las credenciales

![proteg](/assets/img/proteg.png)

<br>

![pagina-1](/assets/img/pagina-1.png)

<br>

Pero si no añadimos credenciales nos deniega el accesso.



![AUTORIZADO](/assets/img/AUTORIZADO.png)

