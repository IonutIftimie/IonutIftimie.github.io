---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Práctica Django"
categories: jekyll update
---
## 1. Crear el directorio del proyecto `mkdir django`:

![mkdir_django](/assets/img/mkdir_django-1612977875806.png)

<br>

## 2. Crear el fichero Dockerfile `vi Dockervile`:

![Dockerfile](/assets/img/Dockerfile-1612977882938.png)

<br>



## 3. Crear el fichero requirements.txt `vi requirements.txt`:

![Requirements](/assets/img/Requirements-1612977895440.png)



<br>

## 4. Crear el archivo docker-compose `vi docker-compose.yml`:



![Docker_Compose_bienx3](/assets/img/Docker_Compose_bienx3-1612977901600.png)



<br>

## 5. Ejecutar el archivo docker-compose `sudo docker-compose run web django-admin startproject composeexample .`

![Docker_Project_ejec](/assets/img/Docker_Project_ejec.png)

<br>

## 6. Cambiar el propietario root al usuario deseado `sudo chown -R $USER:$USER .`:



![Chown_bien](/assets/img/Chown_bien.png)

<br>

## 7. Cambiar los ajustes de la base de datos `compossexample/settings.py`:

![Settings-py_bien](/assets/img/Settings-py_bien.png)

<br>

## 8. Arrancar el servicio `docker-compose up`:

![up](/assets/img/up.png)



<br>

![Django_localhost](/assets/img/Django_localhost.png)