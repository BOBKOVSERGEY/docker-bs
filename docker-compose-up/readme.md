docker compose up

# удалить не используемы контейнеры
docker container prune

# остановить и удалить контейнеры
docker compose down

# пересоздание образа
docker compose up -d --build

# посмотреть логи 
docker logs c049857360e5