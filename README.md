# RaspberryPi  Coding
Template with links to running code on Raspberry Pi

## Install docker 
1. Install docker on Raspberry Pi

```
$ sudo apt-get update
$ sudo apt-get upgrade
$ curl -fsSL test.docker.com -o get-docker.sh && sh get-docker.sh
```

Add the current user to the docker group to avoid needing sudo to run the docker command:
```
$ sudo usermod -aG docker $USER 
```
or just run it for pi user

```
$ sudo usermod -aG docker pi
```

Make sure to log out and back in again. (Only Windows get the grief of restart though)


Now test the install with a quick hello-world run.

```
docker container run hello-world
```

this is more detailed explanation of how to install docker there https://linuxize.com/post/how-to-install-and-use-docker-on-raspberry-pi/

## Install docker-compose


first  Install dependencies
```
sudo apt-get install -y libffi-dev libssl-dev

sudo apt-get install -y python3 python3-pip

sudo apt-get remove python-configparser
```
Then install it
```
sudo pip3 install docker-compose
```


In this tutorial I am using this repo https://github.com/mrcoles/node-react-docker-compose 


what you would need to exec anything , is just clonning the code into the Raspberry Pi 

```
git clone https://github.com/mrcoles/node-react-docker-compose.git
cd node-react-docker-compose 
```

then 

```
docker-compose up
```

docker compose will prep the images for you and run them, then you will be able to edit files and update them.

you can now access the running app from 

RaspberryPI_IP:3000 (Client App)

RaspberryPI_IP:8080/api (Server App)



if you want to run thye images in the background



use 
```
docker-compose up -d
```






Docker on April 7 2020 announced that compose specification are now open

https://www.docker.com/blog/announcing-the-compose-specification/
