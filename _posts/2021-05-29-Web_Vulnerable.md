---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Web vulnerable(bWAPP)"
categories: jekyll update
---

Con la página web vulnerable de bWAPP hay muchas formas de aprovecharlas, algunas de ellas son las siguientes:

## Html Injection

`<h1>Hi</h1>`

![html_injection](/ionut/Imágenes/html_injection.png)



<br>

## XSS

`<script>alert(1)</script>`

![xss_](/ionut/Imágenes/xss_.png)

<br>



## Command injection

`172.0.0.1; cat /etc/passwd;`

![command_injection](/ionut/Imágenes/command_injection.png)

