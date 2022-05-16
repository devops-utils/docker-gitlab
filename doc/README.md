```shell
cd docker
sudo docker-compose up -d

sudo docker-compose -f docker-compose1.yml up -d
sudo docker-compose -f docker-compose1.yml down

sudo docker-compose -f docker-compose1.yml logs -f

sudo docker volume ls
sudo docker volume rm docker_gitlab-data
sudo docker volume rm docker_postgresql-data
sudo docker volume rm docker_redis-data
```