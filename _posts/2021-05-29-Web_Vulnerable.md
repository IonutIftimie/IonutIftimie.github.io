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



![html_injection](/assets/img/html_injection-1622301540726.png)

<br>

## XSS

`<script>alert(1)</script>`

![xss_](/assets/img/xss_.png)

<br>



## Command injection

`172.0.0.1; cat /etc/passwd;`

![command_injection](/assets/img/command_injection.png)