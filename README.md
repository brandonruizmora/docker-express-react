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

Para empezar con el proyecto backend creamos la carpeta _der-api-web_. Dentro del directorio se usara el comando _`npm init`_ para inicializar el proyecto. Luego instalaremos **express y cors**, para poder iniciar nuestra **api**, esto lo haremos con el comando _`npm i express cors`_. Después podemos crear nuestro archivo **index.js** que correra nuestra aplicación. Para verificar que esta funcionando se usara el comando _`node index.js`_. Finalmente verificamos que nuestro backend se este ejecutando correctamente.

![1](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/1.png?raw=true)
![2](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/2.png?raw=true)
![3](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/3.png?raw=true)
![4](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/4.png?raw=true)
![5](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/5.png?raw=true)

## 2. Crear aplicación frontend

Para empezar con el proyecto frontend se usara el comando _`yarn create vite`_ para crear el proyecto. Luego dentro del directorio instalaremos todas las dependencias con el comando _`yarn`_. y Ejecutaremos la aplicación con el comando _`yarn dev`_. y verificamos que nuestro frontend se este ejecutando correctamente.

![6](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/6.png?raw=true)
![7](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/7.png?raw=true)
![8](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/8.png?raw=true)
![9](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/9.png?raw=true)

## 3. Verificar que las 2 aplicaciones se puedan comunicar.

Para verificar que el frontend se pueda comunicar correctamente con el backend utilizaremos _fetch_. Dentro de App.jsx agregaremos una función que haga una petición al api local, cuando se haga clic a un botón, Si la petición se hace correctamente se mostrara un mensaje de alerta y el texto del botón cambiara a la respuesta del api.

![10](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/10.png?raw=true)
![11](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/11.png?raw=true)
![12](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/12.png?raw=true)
![13](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/13.png?raw=true)

## 4. Crear Dockerfile de las 2 aplicaciones

### Dockerfile API

Dentro de la aplicación der-api-web creamos el archivo Dockerfile con los siguiente elementos.

![14](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/14.png?raw=true)

Indicamos la imagen base, creamos el directorio donde se guardara la aplicación, copeamos el contenido de nuestra aplicación local a el directorio creado, definimos el directorio de trabajo, hacemos la instalación de las dependencias, exponemos el puerto que se usara, y finalmente el comando para ejecutar nuestra aplicación.

### Dockerfile UI

Dentro de la aplicación der-api-web creamos el archivo Dockerfile con los siguiente elementos.

![15](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/15.png?raw=true)

Indicamos la imagen base, creamos el directorio donde se guardara la aplicación, copeamos el contenido de nuestra aplicación local a el directorio creado, definimos el directorio de trabajo, hacemos la instalación de las dependencias, exponemos el puerto que se usara, y finalmente el comando para ejecutar nuestra aplicación.

## 5. Crear docker-compose.yml

En la carpeta raiz de nuestros 2 proyectos creamos el archivo docker-compose.yml con los siguientes elementos.

![16](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/16.png?raw=true)

La versión de escritura, los servicios que se usaran, de donde se crearan las imagenes, que nombre tendran el contenedor creado, y que puertos se mapearan.

## 6. Ejecutar Servicios

Para crear las imagenes correspondientes de nuestros proyectos, crear los contenedores, red para comunicarse entre contenedores utilizaremos el comando _`docker compose up`_.

![17](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/17.png?raw=true)

Ahora podemos revisar localhost:3000 para ver nuestro API

![18](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/18.png?raw=true)

También localhost:5173 para ver nuestra UI

![19](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/19.png?raw=true)

## 7. Terminar servicios y borrar imágenes

Para terminar podemos borrar los contenedores y red con el comando _`docker compose down`_. y borrar las imagenes con el comando _`docker image rm`_.

![20](https://github.com/brandonruizmora/docker-express-react/blob/master/imgs/20.png?raw=true)