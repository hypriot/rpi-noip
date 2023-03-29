# rpi-noip

rpi-noip is a docker image of the official [no-ip](http://www.noip.com/) Dynamic DNS Update client 


## Getting started

1. Setup an account in www.noip.com

2. Create a folder in / named noip, for example, `cd / ; sudo mkdir noip` 

3. Run `sudo docker run -ti -v "/noip:/usr/local/etc/" hypriot/rpi-noip noip2 -C`

  This step will ask for your noip credentials and generate the necessary configuration for your container to run. The configuration file will be persisted in the /noip folder.

4. Run `sudo docker run -d -v "/noip:/usr/local/etc/" --restart=always hypriot/rpi-noip` 

  This will start your noip container daemon and it will restart it even if you restart your pi, now you can access your
device anywhere in the world as it will update the DNS automatically


## License

MIT
