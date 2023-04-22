# Docker 

## Requerido

Docker desktop [Download link](https://docs.docker.com/get-docker/)

**o**

Docker ubuntu

Uninstall older versions  `sudo apt-get remove docker docker-engine docker.io containerd runc`

Install last version `sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`

---

## Descripción 

Crear un espacio de trabajo de 2 aplicaciones node. Una aplicación backend en express y otra aplicación frontend en react.

---

## Pasos

1. Crear aplicación backend
2. Crear aplicación frontend
3. Crear Dockerfile de las 2 aplicaciones
4. Crear docker-compose.yml
5. Ejecutar Servicios
6. Terminar servicios y borrar imágenes

---

## 1. Crear aplicación backend

Para empezar con el proyecto de express creamos la carpeta _der-api-web_. Dentro del directorio se usara el comando _`npm init`_ para inicializar el proyecto. Luego instalaremos express y cors, para poder iniciar nuestra api, esto lo haremos con el comando _`npm i express cors`_. Después podemos crear nuestro archivo **index.js** que correra nuestra aplicación. Para verificar que esta funcionando se usara el comando _`node index.js`_. Finalmente verificamos que nuestro backend se este ejecutando correctamente.

![1](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/1.png?raw=true)
![1](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/2.png?raw=true)
![1](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/3.png?raw=true)
![1](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/4.png?raw=true)
![1](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/5.png?raw=true)

## 2. Crear aplicación frontend
## 3. Crear Dockerfile de las 2 aplicaciones
## 4. Crear docker-compose.yml
## 5. Ejecutar Servicios
## 6. Terminar servicios y borrar imágenes
