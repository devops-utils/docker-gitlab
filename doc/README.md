```shell
cd docker
sudo docker-compose up -d

mkdir -p gitlab-data/certs

sudo docker-compose -f docker-compose1.yml up -d
sudo docker-compose -f docker-compose1.yml down

sudo docker-compose -f docker-compose1.yml logs -f

sudo docker exec -it docker_gitlab_1 bash
gitlab-ctl reconfigure
gitlab-rails console
Notify.test_email('noreply@7otech.com','邮件标题','邮件内容').deliver_now

sudo docker exec -it docker_postgresql_1 bash
sudo docker exec -it docker_redis_1 bash

sudo docker volume ls
sudo docker volume rm docker_gitlab-data
sudo docker volume rm docker_postgresql-data
sudo docker volume rm docker_redis-data

http://49.232.6.131:8094/
```