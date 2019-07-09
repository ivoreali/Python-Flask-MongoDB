
## Initial Development Environment to work with Python, Flask and MongoDB

It uses ***Docker-compose***:
Compose is a tool for defining and running complex applications with Docker. With Compose, you define a multi-container application in a single file, then spin your application up in a single command which does everything that needs to be done to get it running.

https://docs.docker.com/compose/install/

After installing Docker and Docker-compose on your machine, you can go to the project main folder and type:

 `$sudo docker-compose up`


**Docker-compose** will build the containers necessary for your environment. Basically there will be two containers, one with Python, Flask and a few modules and another container with MongoDB bound to the first.
The environment structure is as follow:


app/
  
(You need to create a directory /app in your local harddrive. This is where you will keep your app.py Flask file for development.)  

data/

Dockerfiles/

docker-compose-yml


Within the **app** folder, there is an app.py file which is file that starts Flask.

This app.py file is shared with the container, so if you edit it locally on your machine, it will reflect on the container which is running Flask on port 5000.

If everything works fine, you should be able to connect to a simple page (Hello World) at:


http://localhost:5000


the other folders are necessary for:

**data** -> mongodb folder (shared with Mongo's Container)

**Dockerfiles** -> the Dockerfiles which create the containers, any change on each container can be done by editing these files

**docker-compose-yml** -> is the orquestrator that starts building the containers and link them up.






