# Instalación de WordPress usando contenedores Docker y Docker Compose

## PASO 1: INSTALAR DOCKER Y DOCKER COMPOSE
En primer lugar como al crear la maquina no tenemos instalado docker, hemos realizado la instalación con los siguientes comandos:

    sudo apt update

    sudo apt install apt-transport-https ca-certificates curl software-properties-common

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

    sudo apt update

    apt-cache policy docker-ce

    sudo apt install docker-ce

![Texto alternativo](/img/cap5.png)

Como podemos ver el servicio de docker esta funcionando correctamente.

## PASO 2: CLONAR REPOSITORIO CON LO NECESARIO

A continuacion para tener los archivos necesarios para el despliegue de worpress con docker compose, haremos un git clone del repositorio con todo lo necesario (AVISO:Previamente hemos realizado un fork del repositorio de nuestro profesor)

    git clone https://github.com/anarodriguezm/docker-compose-playground.git

Nos moveremos al directorio que se nos ha descargado:

    cd docker-compose-playground/

Y en este caso lo necesario para la actividad se encuentra en la siguiente ruta:

    cd example-15-wordpress-mariadb/

Una vez nos encontramos aqui realizaremos un docker compose para desplegar los servicios para wordpress,mariadb y phpmyadmin

![Texto alternativo](/img/cap6.png)

Como podemos ver estarian ya en ejecucion los servicios, con docker ps podemos ver tambien que se ha levantado el contenedor.

![Texto alternativo](/img/cap7.png)

Ahora una vez el sitio web se encuentre en ejecucion procederemos a la instalacion de Wordpress

![Texto alternativo](/img/compose1.png)

Una vez terminada la configuración, tendremos acceso a nuestro panel de configuracion de Wordpress.

![Texto alternativo](/img/compose2.png)

Como podemos observar tendriamos un menu lateral en el que podremos configurar nuestro sitio web a nuestro gusto y si nos vamos arriba a la derecha podremos visitarlo y observar los cambios realizados.

![Texto alternativo](/img/compose4.png)

Esta sería la pagina por defecto que nos despliega Wordpress en editar sitio podriamos modificarla a nuestro gusto.

![Texto alternativo](/img/compose5.png)
