sometimes we need multiple compose files

PS D:\docker_pract\exercise14> docker compose -f docker-compose.dev.yml up -d
[+] Building 0.0s (0/0)                                                                                                                                                docker:default
[+] Running 3/3
 ✔ Network exercise14_default  Created                                                                                                                                           0.1s 
 ✔ Container exercise14-db-1   Started                                                                                                                                           0.2s 
 ✔ Container exercise14-web-1  Started    


 PS D:\docker_pract\exercise14> docker compose -f docker-compose.dev.yml down 
[+] Running 3/3
 ✔ Container exercise14-web-1  Removed                                                                                                                                           0.6s 
 ✔ Container exercise14-db-1   Removed                                                                                                                                           1.7s 
 ✔ Network exercise14_default  Removed       