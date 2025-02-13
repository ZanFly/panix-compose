Docker compose for Apache Guacamole, written for deploying with Portainer.

TOTP Authentication enabled.

This compose file create 3 docker container with:

#

mysql:latest - Database for Guacamole

guacamole/guacd:latest - client managing connection with local hosts

guacamole/guacamole:latest - The web frontend

#

This assumes there's a MACVlan interface already deployed with range 192.168.0.0/24

You can modify to fit with your MACVlan configuration or exposing only web frontend port 8080.

Also, create a bridge "net" for communications between containers.

#

There's also an AddOn with adminer:latest can be useful for first db deploy or if you want to see/modify db data.

#

To do before use:

1- Check network configuration

2- CHANGE PASSWORDS (mysql root, guacamole db user)

3- Change data folder for binding your favourite "AppData" folder, or have volumes for saving data
