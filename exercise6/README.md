docker-compose

PS D:\docker_pract\exercise6> docker compose config
name: exercise6
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
    name: exercise6_default


PS D:\docker_pract\exercise6> docker compose up -d
[+] Running 8/8
 ✔ rcache 7 layers [⣿⣿⣿⣿⣿⣿⣿]      0B/0B      Pulled                                                            11.5s 
   ✔ c926b61bad3b Pull complete                                                                                 1.8s 
   ✔ d37d50d32a98 Pull complete                                                                                 1.3s 
   ✔ cdf33658b38c Pull complete                                                                                 2.9s 
   ✔ 39333280c8c6 Pull complete                                                                                 3.9s 
   ✔ c105db640f3f Pull complete                                                                                 3.1s 
   ✔ 4f4fb700ef54 Pull complete                                                                                 3.9s 
   ✔ f12f505e3a3c Pull complete                                                                                 4.8s 
[+] Building 0.0s (0/0)                                                                               docker:default
[+] Running 3/3
 ✔ Network exercise6_default     Created                                                                        0.2s 
 ✔ Container exercise6-rcache-1  Started                                                                        0.6s 
 ✔ Container exercise6-web-1     Started     