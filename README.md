使用Docker一键部署:
```
docker run -d --restart always -p 8090:80 --name sub-web ly88321/sub-web
```
或使用docker compose
```yaml
name: sub-web
services:
    sub-web-modify:
        restart: always
        privileged: false
        ports:
            - 8090:80
        container_name: sub-web
        image: ly88321/sub-web
```
运行docker compose: `docker compose up -d`
