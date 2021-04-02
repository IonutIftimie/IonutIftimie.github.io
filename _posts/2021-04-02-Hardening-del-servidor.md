---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Hardening del servidor"
categories: jekyll update
---

## P1. Deshabilitar autoindex

Con `a2dismod --force autoindex` se puede deshabilitar el autoindexado:

![autoindex](/assets/img/autoindex.png)

<br>



![autoindexoff2](/assets/img/autoindexoff2.png)

Y para deshabilitar la versión de apache se soluciona con los modulos `ServerTokens Prod` y `ServerSignature Off`.

<br>



![server-signature](/assets/img/server-signature.png)



<br>

![curl2](/assets/img/curl2.png)

<br>



## P1. HSTS

Para solo permitir solo tráfico ssl(https) se añadiria el siguiente modulo.

![header-ssl](/assets/img/header-ssl.png)

<br>



![ssl](/assets/img/ssl.png)

## P1. CSP

Para aplicar esta capa de seguridad simplemente se añadira el siguiente modulo.

<br>

![header-set](/assets/img/header-set.png)

<br>

## P2. WAF

Se descarga e instala modsecurity y se crea(renombra) el fichero de cofiguración.

![waf2](/assets/img/waf2.png)

<br>

![waf](/assets/img/waf.png)

<br>



## P3. OWASP

Clonamos el repositorio de owasp y añadimos los ficheros de configuración y reglas

![owasp-dockerfile](/assets/img/owasp-dockerfile.png)

<br>

Y por ultimo comprobamos

<br>

![curl(owasp)](/assets/img/curl(owasp).png)

<br>

