---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "File Upload"
categories: jekyll update
---

## File Upload

Realizaremos un reverse shell con DVWA, descargamos el fichero de reverse shell de [aquí](https://raw.githubusercontent.com/pentestmonkey/php-reverse-shell/master/php-reverse-shell.php#)

y modificamos la ip por la nuestra.

![reverse1](/assets/img/reverse1.png)

<br>

La subimos a la pagina vulnerable el reverse shell.

![reverse2](/assets/img/reverse2.png)

<br>

Nos quedamos a la espera de una conexión.

![reverse3](/assets/img/reverse3.png)

<br>

Y finalmente se establece la conexión.

![reverse4](/assets/img/reverse4.png)