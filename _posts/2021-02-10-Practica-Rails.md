---
typora-copy-images-to: ../assets/img/
typora-root-url: ../
layout: post
title:  "Práctica Rails"
categories: jekyll update
---

## 1. Crear el directorio del proyecto `mkdir rails`:

![Mkdir_Rails](/assets/img/Mkdir_Rails.png)

<br>

## 2. Crear el fichero Dockerfile `vi Dockerfile`:



![Dockerfile_bien](/assets/img/Dockerfile_bien.png)



<br>

## 3. Crear el fichero Gemfile `vi Gemfile`:



![Gemfile](/assets/img/Gemfile.png)

<br>

## 4. Crear el fichero Gemfile.lock `touch Gemfile.lock`:

![Gemfile-lock](/assets/img/Gemfile-lock.png)



<br>

## 5. Crear el archivo Entrypoint `vi Entrypoint`:



![Entrypoint](/assets/img/Entrypoint.png)



<br>

## 6. Crear el archivo docker-compose.yml `vi docker-compose.yml`:



![Docker_compose-yml_bien](/assets/img/Docker_compose-yml_bien.png)



<br>

## 7. Generar el esqueleto de Rails `docker-compose run --no-deps web rails new . --force --database=postgresql`:



![Docker_compose_run](/assets/img/Docker_compose_run-1613498075658.png)



<br>

## 8. Cambiar el propietario `sudo chown -R $USER:$USER .`:



![Chown](/assets/img/Chown-1613497542119.png)

<br>



## 9. Contruir la imagen `sudo docker-compose build`:

![Build](/assets/img/Build.png)



<br>



## 10.  Reemplazar el contenido de `config/database.yml`:

![databaseconfig_bien](/assets/img/databaseconfig_bien.png)



<br>



## 11.  Iniciamos la app `docker-compose up`:



![up](/assets/img/up-1613497877519.png)



<br>



## 12. Crear un base de datos `docker-compose run web rake db:create`:

![database_run](/assets/img/database_run.png)

<br>



## 13. Comprobación `localhost:3000`:



![localhost-3000](/assets/img/localhost-3000-1613498040818.png)