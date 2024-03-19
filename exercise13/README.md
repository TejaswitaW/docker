we can give order of container creation, there can be contianers dependent on each other
means startup and shutdown order we can give


PS D:\docker_pract\exercise13> docker compose up -d
[+] Building 0.0s (0/0)                                                                                                                        docker:default
[+] Running 4/4
 ✔ Network exercise13_proj_tk_network  Created                                                                                                           0.2s 
 ✔ Container exercise13-db-1           Started                                                                                                           0.1s 
 ✔ Container exercise13-rcache-1       Started                                                                                                           0.2s 
 ✔ Container exercise13-web-1          Started   


 PS D:\docker_pract\exercise13> docker compose down --volumes
[+] Running 4/4
 ✔ Container exercise13-web-1          Removed                                                                                                           0.5s 
 ✔ Container exercise13-db-1           Removed                                                                                                           2.1s 
 ✔ Container exercise13-rcache-1       Removed                                                                                                           0.6s 
 ✔ Network exercise13_proj_tk_network  Removed     