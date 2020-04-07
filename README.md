# RaspberryPi-coding
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




