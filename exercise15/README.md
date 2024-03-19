How to use own image in compose

PS D:\docker_pract\exercise15> docker compose up -d
[+] Building 1.0s (6/6) FINISHED                                                                                                               docker:default
 => [app internal] load build definition from Dockerfile                                                                                                 0.2s
 => => transferring dockerfile: 118B                                                                                                                     0.0s
 => [app internal] load .dockerignore                                                                                                                    0.2s
 => => transferring context: 2B                                                                                                                          0.0s
 => [app internal] load metadata for docker.io/library/alpine:latest                                                                                     0.0s
 => [app 1/2] FROM docker.io/library/alpine                                                                                                              0.1s
 => [app 2/2] WORKDIR /app                                                                                                                               0.1s 
 => [app] exporting to image                                                                                                                             0.2s 
 => => exporting layers                                                                                                                                  0.2s 
 => => writing image sha256:b3349ce262625389d0efe826cb28014af47aefd6f53c55ff3e1babf045750e2b                                                             0.0s 
 => => naming to docker.io/library/exercise15-app                                                                                                        0.0s 
[+] Running 4/4
 ✔ Network exercise15_default  Created                                                                                                                   0.1s 
 ✔ Container exercise15-db-1   Started                                                                                                                   0.4s 
 ✔ Container exercise15-app-1  Started                                                                                                                   0.3s 
 ✔ Container exercise15-web-1  Started    