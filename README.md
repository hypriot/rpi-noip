# rpi-noip

rpi-noip is a docker image of the official [no-ip](http://www.noip.com/) Dynamic DNS Update client 


## Getting started

1. Setup an account in www.noip.com

2. Run `docker run -ti -v "noip:/usr/local/etc/" hypriot/rpi-noip noip2 -C`

  This step will ask for your noip credentials and generate the necessary configuration for your container to run

3. Run `docker run -v "noip:/usr/local/etc/" -d --restart=always hypriot/rpi-noip` 

  This will start your noip container daemon and it will restart it even if you restart your pi, now you can access your
device anywhere in the world as it will update the DNS automatically


## Buy us a beer!

This FLOSS software is funded by donations only. Please support us to maintain and further improve it!

<a href="https://liberapay.com/Hypriot/donate"><img alt="Donate using Liberapay" src="https://liberapay.com/assets/widgets/donate.svg"></a>


## License

MIT
