---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Práctica Nginx con Docker"
categories: jekyll update
---



## Nginx con Docker

<br>

## 1. Instalar Nginx:

![nginx1](/assets/img/nginx1.png)

```
docker run --rm -d -p 8080:80 --name web nginx
```

<br>

![NgxDocker2](/assets/img/NgxDocker2.png)

***Parar contenedor***

![NgxDocker3](/assets/img/NgxDocker3.png)

<br>

<br>

## 2. Añadir HTML personalizado:





![NgxDocker4](/assets/img/NgxDocker4.png)

<br>

<br>

## 3. Crear volumen y montar directorio local: 

![NgxDocker5](/assets/img/NgxDocker5.png)

```
sudo docker run --rm -d -p 8080:80 --name web -v ~/Documentos/nginx/site-content:/usr/share/nginx/html nginx
```

<br>

![NgxDocker6](/assets/img/NgxDocker6.png)

<br>

<br>



## 4. Crear una imagen personalizada:

## Crear el fichero con el siguiente contenido:



![NgxDocker7](/assets/img/NgxDocker7.png)

```
FROM nginx:latest
COPY ./site-content/index.html /usr/share/nginx/html/index.html
```



## Construir imagen:

![NgxDocker8](/assets/img/NgxDocker8.png)

```
sudo docker build -t webserver .
```

<br>

<br>

## Ejecutar la imagen (Sin crear un volumen):

![NgxDocker9](/assets/img/NgxDocker9-1612362094157.png)

```
sudo docker run --rm -d -p 8080:80 --name web webserver
```

