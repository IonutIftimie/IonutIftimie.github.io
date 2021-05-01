---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Evitar ataque DoS"
categories: jekyll update
---

#### 1. Instalar `mod-evasive` y sus dependencias si no se tiene instalado :

<code>sudo apt install aptitude -y</code>

<code>sudo aptitude install libapache2-mod-evasive -y</code>

![Captura de pantalla_2021-05-01_20-11-06](/assets/img/Captura de pantalla_2021-05-01_20-11-06.png)

<br>

#### 2. Modificar el archivo `evasive.conf` para que quede así:

![evasive-conf](/assets/img/evasive-conf.png)

<br>

#### 3. Creamos un directorio para los logs y cambiamos propietario:

![mkdir-chonw](/assets/img/mkdir-chonw.png)

<br>

#### 4. Reiniciamos apache2:

![restart](/assets/img/restart.png)

<br>

#### 5. Iniciamos el test del propio `mod-evasive`:

<code>perl /usr/share/doc/libapache2-mod-evasive/examples/test.pl</code>

![test-pl](/assets/img/test-pl.png)

<br>

#### 6. Intentamos realizar el ataque y revisamos los logs:

<code>ab -n100 -c5 http://127.0.0.1/index.html:80</code>

![testeo](/assets/img/testeo.png)

<br>

![error-log](/assets/img/error-log.png)

<br>

![acces-log](/assets/img/acces-log.png)

