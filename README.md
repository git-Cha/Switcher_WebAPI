#  Install Switcher WebAPI on hassio (vmware image)

in order to work with containers on hassio, you need to install an official add on from the add-on store :
![image](https://user-images.githubusercontent.com/61497622/81860682-bf343680-956f-11ea-9d49-b0fe16c081b3.png)
 
 after installtion complited, you need to disable Protection mode:
![image](https://user-images.githubusercontent.com/61497622/81860706-c8250800-956f-11ea-8f66-c6dec7c16b85.png)

and restart hassio:
![image](https://user-images.githubusercontent.com/61497622/81860721-ce1ae900-956f-11ea-9f61-86f69c5d1637.png)

open Portainer addon, choose "images", write the name of the image and click import:

image name:       tomerfi/switcher_webapi:latest
![image](https://user-images.githubusercontent.com/61497622/81860742-d6732400-956f-11ea-981e-ab7422490dea.png)

Building container:

choose "add contanier:

![image](https://user-images.githubusercontent.com/61497622/81860755-db37d800-956f-11ea-9edc-8fa220d80c29.png)

enter the following details:

container_name: switcher_webapi

image: tomerfi/switcher_webapi:latest

restart: unless-stopped

network=host


env_vars

CONF_DEVICE_IP_ADDR=192.168.48.50 [switcher ip]

CONF_PHONE_ID=0000

CONF_DEVICE_ID=xxxxx

CONF_DEVICE_PASSWORD=12345678

CONF_THROTTLE=5.0


print screens:

![image](https://user-images.githubusercontent.com/61497622/81860779-e5f26d00-956f-11ea-855e-ec2d9fb5add4.png)

![image](https://user-images.githubusercontent.com/61497622/81860791-ea1e8a80-956f-11ea-978d-9c5b9b4313a5.png)

![image](https://user-images.githubusercontent.com/61497622/81860805-ee4aa800-956f-11ea-8530-4b59d7a8a2f5.png)

![image](https://user-images.githubusercontent.com/61497622/81860811-f1459880-956f-11ea-9525-af6178adcd4f.png)

at the end, press: ![image](https://user-images.githubusercontent.com/61497622/81860844-fd315a80-956f-11ea-88f2-103414d657b9.png)

makeing sure that the container is up and running:

![image](https://user-images.githubusercontent.com/61497622/81860860-028ea500-9570-11ea-8c05-d964698a97dc.png)

follow Dima's guide and set configuration.yaml:

https://github.com/dmatik/homeassistant-config/wiki/Switcher-integration-using-WebAPI

examples:

![image](https://user-images.githubusercontent.com/61497622/81860888-0f12fd80-9570-11ea-9a77-b9809fda7586.png)

the ip address of this hassio instant is 192.168.48.35

![image](https://user-images.githubusercontent.com/61497622/81860899-15a17500-9570-11ea-98fa-56b765969d50.png)
![image](https://user-images.githubusercontent.com/61497622/81860907-1803cf00-9570-11ea-92de-49fa43126cf1.png)
![image](https://user-images.githubusercontent.com/61497622/81860918-1c2fec80-9570-11ea-9c5f-6795ec06b9b9.png)

by adding simpale entity card you can see:

![image](https://user-images.githubusercontent.com/61497622/81860928-218d3700-9570-11ea-90c6-79832af4e21e.png)



בהצלחה!
תודה לדימה ולתומר  :)
