# Docker_Shpora

### - Собрать контейнер 
```
docker build -t <name> .
```
### - Пооднять контейнер в фоновом режиме
```
docker run -d <image_name>
```
### - Запукск контейнера из образа <image_name>
```
docker run -d --name mн_container <image_name>
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

### Добваить внутрь сети контейнер
```
docker network connect <network name> <container name>
```

### - Опустить все запущенные контейнеры 
```
docker stop $(docker ps -a -q)
```

### - Опустить все запущенные контейнеры 
```
docker exec -it <container_name/container_id> /bin/bash
```

### - Для остановки контейнеров Docker:
```
sudo docker compose down -v      # с их удалением
sudo docker compose stop         # без удаления
```

### - Для просмотра id контейнера
```
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container_name_or_id>
```
