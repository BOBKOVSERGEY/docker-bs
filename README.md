# версия докер и engine
docker version

# список запущенных контейнеров и остановленных контейнеров
docker ps -a

# список запущенных контейнеров
docker ps

# список всех образов
docker images

# создает и запускает контейнер
docker run hello-world

# удалить контейнер
docker rm bc26b5b6cdbe

# docker run -it busybox
hostname
hostname -i
ping 8.8.8.8

# finished process
exit

# delete all containers that have been left behind
docker container prune

# nginx
docker run nginx

# running containers in the background
docker run -d nginx

# view details of the entire container
docker container inspect 5f7e4d4f8220

# filtering 
docker container inspect 5f7e4d4f8220 | grep IPAddress

# stop container use container id or name 
docker stop epic_williams

# we launch an additional process in an already running container it - интереактивнй терминал use container id or name
docker exec -it 5f7e4d4f8220 bash

# get ip address in bash
hostname -i

# path to nginx html
cd /usr/share/nginx/html

# read file
cat index.html

# create container with custom name
docker run -d --name my_nginx nginx


# publishing container ports (-p публикация порта, 8080 - внешний порт, 80 - порт внутри контейнера)
docker run -d -p 8080:80 nginx

# stop multiple containers
docker stop 838a9321d041 1f4386a1bd13

# absolute path
echo ${PWD}

# mapping volumes (-v подключение тома ${PWD} -путь к локальной папке, /usr/share/nginx/html - путь внутри контейнера)
docker run -d -p 8080:80 -v ${PWD}:/usr/share/nginx/html nginx

# automatic container removal (--rm)
docker run -d -p 8080:80 -v ${PWD}:/usr/share/nginx/html --rm nginx

# splitting commands into lines
docker run \
    -d \
    -p 8080:80 \
    -v ${PWD}:/usr/share/nginx/html \
    --rm \
    nginx


# интерактивный терминал 
docker exec -t a71868ead693 sh