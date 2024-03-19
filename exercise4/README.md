1. For example this is my project, I want to mount this project in container,because i want to run in Docker because in this operating system python is not installed.
I have created one image and using that image i will create container and I will run this project.
I want to do mounting, becasue this code will go there then it will run.

First I will copy path to my project folder.
$ docker run --name tk-python -itd -v D:\docker_pract\exercise3:/myapp python
Here, myapp will get created in container,these two folders will get mapped,python is the image name, then,

PS C:\Users\pytho> docker exec -it tk-python bash
root@85375acede5e:/# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  myapp  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@85375acede5e:/# cd myapp/
root@85375acede5e:/myapp# python app.py
Hello Kartiki
root@85375acede5e:/myapp#

I this way project is in host but we are running it in docker container,
If you do any changes to project, those will get reflected in mapped folder.

I this way we can mount our project on host in docker container.

We have seen how, host to container data is getting shared 

Next we will see, between container data is getting shared using volume
First create volume then mount to container, c1 and c2 are container names
$ docker volume create myvol
$ docker run --name cl -itd -v myvol:/myapp python 
$ docker run --name c2 -itd -v myvol:/myapp1 python 

If you do changes in myapp or myapp1 => those will get reflected in both folders.


volume is independent of container , if you delete container volume will remain as it is

Create container with volume
$ docker run --name c1 -itd -v /myvol python ==> give some random name to volume
This volume you can share as follows,
$ docker run --name c2 -itd --volume-from c1 python  => this approach is not recommended,here
volume is not independent , here volume is depenedent on container 1 volume, if that contianer is deleted volume will get deleted, then for c2 there will not be volume.







