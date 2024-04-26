# Docker_Shpora

### - Пооднять контейнер в фоновом режиме 
```
docker run -d <image_name>
```

### - Поднять орекстр в фоновом режиме 
```
docker-compose -f <compose_name.yml> up -d
```

### - Проверить все запущенныые контейнеры 
```
docker ps
```

### - Создать docker network 
Это нужно что бы контейнеры могли "общаться" с друг другом
```
docker network create my-network
```

### - Проверить какие контейнеры есть в сети докер 
```
docker network inspect <network_name>
```

### - Опустить все запущенные контейнеры 
```
docker stop $(docker ps -a -q)
```
### - Для остановки контейнеров Docker:
```
sudo docker compose down -v      # с их удалением
sudo docker compose stop         # без удаления
```
