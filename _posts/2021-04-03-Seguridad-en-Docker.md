---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Seguridad en Docker"
categories: jekyll update
---

## 1. Seguridad en Host

Para la seguridad en host se deben añadir los usuario que deban tener permiso para lanzar contenedores al grupo docker.



![seguridad-host](/assets/img/seguridad-host.png)

<br>

## 2. Seguridad en el demonio

Para impedir que usuarios pudan modificar la configuración y que no puedan ver el socket se añade(o se crea) el archivo `daemon.json` lo siguiente:

![daemon-json](/assets/img/daemon-json.png)

<br>

## 3. Seguridad en contenedores

Si se quiere limitar los recursos de un contenedro se usa el parametro `--cpus`

![seguridad-en-docker-1](/assets/img/seguridad-en-docker-1.png)

<br>

## 4 . Privilegios

Si utilizamos un usuario ( 4400) que no tiene privilegios para realizar acciones que necesite tener permisos nos aparecera un mensaje de error.

![docker-privilegios](/assets/img/docker-privilegios.png)



![docker-mount-non-privileged](/assets/img/docker-mount-non-privileged.png)

<br>

Pero para poder realizar esta acciones se debera usar el parametro`--privileged`



![docker-mount-privileged](/assets/img/docker-mount-privileged.png)

<br>

## 5. Escaneo pasivo de vulneravilidades

Para realizar un escaneo de una imagen se utilizara `trivy`  y la imagen `wordpress:beta-5.7-RC1-php7.4`

![trivy-command](/assets/img/trivy-command.png)





![wordpress-beta-5-7-RC1-php-7-4](/assets/img/wordpress-beta-5-7-RC1-php-7-4.png)