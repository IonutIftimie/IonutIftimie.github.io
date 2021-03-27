---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Validación de entradas"
categories: jekyll update
---

## 1. Mitigar XSS

Para evitar esto utilizamos specialchar.

![peps-post-mejorado](/assets/img/peps-post-mejorado.png)

<br>

## 2. Autenticación con sesiones

Para acceder mediante usuario/contraseña crearemos el siguiente fichero.

![peps-post-mejorado](/assets/img/peps-post-mejorado-1616346722351.png)

<br>

## 3. Robo de sesion

Para relizar esto primero necesitarmeos crear los archivos php y que la victima los visite despues de "logearse".

 ![peps-robo-de-sesion](/assets/img/peps-robo-de-sesion.png)

 <br>

![peps-post-hackeada](/assets/img/peps-post-hackeada.png)

 <br>

Ahora lo comprobamos.

![session-robada](/assets/img/session-robada.png)

<br>

![mario](/assets/img/mario.png)

<br>

## 4. Evitar robo de sesión

Para evitar esto añadiremos esta linea fichero de sesion `ini_set( 'session.cookie_httponly', 1 );`

![login-mejorado](/assets/img/login-mejorado.png)

<br>

## 5. Control de acceso

Para implementar un control de acceso se tendria modificar el archivo de login de sesion y crar tres ficheros mas.

![login2](/assets/img/login2.png)

<br>

![perfil](/assets/img/perfil.png)

<br>

![admin](/assets/img/admin.png)

<br>

![no-autorizado](/assets/img/no-autorizado.png)

<br>

## 6. CSRF (Corss Site Request Frogery)

Para realizar un este tipo de XSS, se necesita crear los siguientes archivos:

por parte de "evil"

![hackada-crsf](/assets/img/hackada-crsf.png)

<br>

y la victima

![transfer](/assets/img/transfer.png)

<br>

danto como resultado

![hackeada-csrf](/assets/img/hackeada-csrf.png)



<br>

## 7. Redirigir a otra web

se necistara crear el siguiente archivo en el host "evil".



![redireect](/assets/img/redireect.png)



![hackeada-redirect](/assets/img/hackeada-redirect.png)