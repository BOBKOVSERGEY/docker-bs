# WORKDIR - путь к папке внутри образа



COPY . . мы копируем из текущий папки компьютера в корневую папку внутри образа /app

# создать образ указываем путь к Dockerfile -t создание тега 
docker build . -t my-calendar

# создание контейнера на основе образа
docker run -it my-calendar

# проверить список запущенных контейнеров
docker ps

# docker build . -t my-calendar:2.0.0

# CMD ["python", "main.py"] - какой процесс запускать при созданиие контейнера

# зайти в оболочку контейнера 
docker exec -t bf0fd2195ac9 sh