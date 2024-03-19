using config file

PS D:\docker_pract\exercise9> docker compose config
name: exercise9
services:
  db:
    environment:
      MYSQL_ROOT_PASSWORD: "12345"
    image: mysql
    networks:
      default: null
  rcache:
    image: redis:6.0-alpine3.18
    networks:
      default: null
  web:
    image: nginx
    networks:
      default: null
networks:
  default:
    name: exercise9_default