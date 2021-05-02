---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Laboratorios(SQL_Injection)"
categories: jekyll update
---

#### 1. Obtener datos ocultos:

​	Si queremos mostrar los datos ocultos de la siguiente pagina web.

![lab-1-1](/assets/img/lab-1-1.png)

<br>

Simplemente añadiendo en la URL <code>'+OR+1=1--</code> nos mostraria todos los datos ocultos.

![lab-1-2](/assets/img/lab-1-2.png)

<br>

![lab-1-3](/assets/img/lab-1-3.png)

<br>

#### 2. Subvertir la funcionalidad de la pagina web

Sabiendo un nombre de usuario se puede intentar iniciar sesión sin saber la contraseña, para ello en este caso el usuario seria `"administrator"` y le añadimos `'--` podriamos iniciar sesion (`administrator'--`).

![lab-2-1](/assets/img/lab-2-1.png)

<br>

![lab-2-2](/assets/img/lab-2-2.png)

<br>

![lab-2-3](/assets/img/lab-2-3.png)

<br>

#### 3. Determinar el numero de columnas

​	Si queremos determinar el numero de columnas de una tabla se puede hacer añadiendo en la URL <code>'+UNION+SELECT+NULL--</code> añadiendo tantos `NULL` como columnas hay.



![lab-3-1](/assets/img/lab-3-1.png)

<br>![lab-3-2](/assets/img/lab-3-2.png)

<br>

![lab-3-3](/assets/img/lab-3-3.png)

<br>![lab-3-5](/../../Escritorio/lab-inje-sql/lab-3-5.png)

<br>

​	O tambien se puede utilizando <code>'+ORDER+BY+3--</code> incrementando el numero/disminuyedo segun la columnas que tenga.



![lab-3-4](/assets/img/lab-3-4.png)

<br>![lab-3-5](/assets/img/lab-3-5-1619957790032.png)

<br>

#### 4. Determinar el tipo y la version



Para que nos muestre la version de la base de datos primero determinamos determinamos el número de columnas y si contienen texto.

![lab-4-1](/assets/img/lab-4-1.png)

Para ello añadimos la siguiente inyección en la URL `'+UNION+SELECT+'abc','def'+FROM+dual--`

![lab-4-2](/assets/img/lab-4-2.png)



<br>

![lab-4-3](/assets/img/lab-4-3.png)

<br>

Ya sabiendo esto usamos esta peticion a la base de datos <code>'+UNION+SELECT+BANNER,+NULL+FROM+v$version--</code> para que nos devuelva la versión

![lab-4-4](/assets/img/lab-4-4.png)

<br>

![lab-4-5](/assets/img/lab-4-5.png)

<br>

![lab-4-6](/assets/img/lab-4-6.png)