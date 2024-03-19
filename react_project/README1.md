Check inside the container

PS D:\docker_pract\react_project\chat-app-proj> docker compose -f docker-compose.dev.yml exec react-project-dev bash
root@688b61e0c5e8:/react-project# ls
Dockerfile.dev  README.md  docker-compose.dev.yml  index.html  node_modules  package-lock.json  package.json  public  src  vite.config.js
root@688b61e0c5e8:/react-project#

our project and continaer node_modules folders are different-in host it is win32
root@688b61e0c5e8:/react-project/node_modules# cd @esbuild
root@688b61e0c5e8:/react-project/node_modules/@esbuild# ls
linux-x64
root@688b61e0c5e8:/react-project/node_modules/@esbuild#