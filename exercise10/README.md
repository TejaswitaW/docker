setting service profile and on that you can apply command
here, from our compose while when run up command only web and db service will run, becasue for redis we set profile we told to not to run, it will not default run

PS D:\docker_pract\exercise10> docker compose config
name: exercise10
services:
  db:
    environment:
      MYSQL_ROOT_PASSWORD: "12345"
    image: mysql
    networks:
      default: null
  web:
    image: nginx
    networks:
      default: null
networks:
  default:
    name: exercise10_default   

  To run redis manually we have to write,we have enabled it,then we can see its output also
  PS D:\docker_pract\exercise10> docker compose --profile rediscache config 
name: exercise10
services:       
  db:
    environment:
      MYSQL_ROOT_PASSWORD: "12345"
    image: mysql
    networks:
      default: null
  rcache:
    profiles:
      - rediscache
    image: redis:6.0-alpine3.18
    networks:
      default: null
  web:
    image: nginx
    networks:
      default: null
networks:
  default:
    name: exercise10_default


it havent created container for redis
PS D:\docker_pract\exercise10> docker compose up -d 
[+] Building 0.0s (0/0)                                                                               docker:default
[+] Running 3/3
 ✔ Network exercise10_default  Created                                                                          0.1s 
 ✔ Container exercise10-web-1  Started                                                                          0.2s 
 ✔ Container exercise10-db-1   Started    
 
 By following command, now it will run redis container too
 PS D:\docker_pract\exercise10> docker compose --profile rediscache  up -d      
[+] Building 0.0s (0/0)                                                                                                      docker:default
[+] Running 4/4
 ✔ Network exercise10_default     Created                                                                                              0.1s 
 ✔ Container exercise10-rcache-1  Started                                                                                              0.2s 
 ✔ Container exercise10-web-1     Started                                                                                              0.2s 
 ✔ Container exercise10-db-1      Started     

To stop remove, we have to do
 PS D:\docker_pract\exercise10> docker compose down --volumes
[+] Running 3/2
 ✔ Container exercise10-db-1   Removed                                                                                                 1.3s 
 ✔ Container exercise10-web-1  Removed                                                                                                 0.5s 
 ! Network exercise10_default  Resource is still in use                                                                                0.0s 
PS D:\docker_pract\exercise10> docker compose --profile rediscache  down --volumes
[+] Running 2/2
 ✔ Container exercise10-rcache-1  Removed                                                                                              0.5s 
 ✔ Network exercise10_default     Removed   