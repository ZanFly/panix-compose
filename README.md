Docker compose for Apache Guacamole, written for deploying with Portainer.
This compose file create 3 docker container with:

mysql:latest - Database for Guacamole
guacamole/guacd:latest - client managing connection with local hosts
guacamole/guacamole:latest - The web frontend

This assumes there's a MACVlan interface already deployed with range 192.168.0.0/24
You can modify to fit with your MACVlan configuration or exposing only web frontend.

There's also an AddOn with adminer:latest can be useful for first db deploy or if you want to see/modify db data.
