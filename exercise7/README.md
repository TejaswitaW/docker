Seperate environment variables and use it in compose file

PS D:\docker_pract\exercise7> docker compose config
name: exercise7
services:      
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
    name: exercise7_default