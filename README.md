# MesosDns
#MesosDns Dockerfile for Code Motion workshop

This repo modifies slightly the official mesosphere/mesosdns Dockerfile adding the mesosDns config file to the image.

* First of all, clone this repo and replace the tag HOST_IP by your HOST IP in the config.json file.

If you are running on mac like me, you might be using Docker-Machine. Instead of using localhost, you must use the IP of your host which can be retrieved via : 

```
docker-machine ls
perso    *        virtualbox   Running   tcp://192.168.99.100:2376
```

In order to replace the tag by your HOST IP you can use sed command :

```
sed -i -e 's/HOST_IP/192.168.99.100/g' config.json
```

* Build the Docker image

```
docker build -t mesosDns .
```
 
