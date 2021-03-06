# Curs-Domotica-Radiofreq-2022


1. [Presentació i introducció](https://github.com/jnogues/Curs-Domotica-Radiofreq-2022/blob/main/cursRadioFreqEstiu2022.pdf).
2. Tecnologies via radio: Wifi, Bluetooth, [Z-Wave](https://www.z-wave.com/), LoRa (LoRaWan) i  Zigbee (Thread-Matter).
3. Avantatges i desavantatges de cada tecnologia.
4. Topologia dels sistemes. Connexió al núvol.
5. Dispositius comercials Wifi:
    * Shelly, SonOff, Tuya, Simon 270.
6. Dispositius comercials Z-Wave:
    * Simon 100.
7. Dispositius comercials Zigbee:
    * Relació entre Zigbee, Thread, Matter i CSA.
    * Ikea Tradfri.
    * Aqara Xiaomi.
    * Valena next with netatmo. 
    * Lidl.
8. Assistents de veu.
9. Configuració i muntatge de dispositius Shelly. Aplicació mòbil i servidor web. 
10. Configuració i muntatge de dispositius SonOff. Aplicació mòbil.
#### Bonus Track
11. Integració en Hub domòtic: Home Assistant.
12. Instal.lació de Home Assistant: En Raspberry Pi, màquina virtual o ordinador amb Debian.
13. Configuracions inicials. Descoberta de nous dispositius.
14. Dispositius DIY esp8266 i esp32 amb esphome.


## Recursos
### Shelly plus 
* [Knowledge base](https://shelly.cloud/knowledge-base/devices/).
#### [Plus 1](https://shelly.cloud/knowledge-base/devices/shelly-plus-1/)
* [Guia d'aplicació del Shelly Plus 1](https://shelly.cloud/documents/user_guide/shelly_plus_1_app.pdf).
* [Guia d'usuari del Shelly Plus 1](https://shelly.cloud/documents/user_guide/Shelly_Plus-1_multilanguage_v09_web.pdf).
#### [Plus 1 PM](https://shelly.cloud/knowledge-base/devices/shelly-plus-1pm/)
* [Guia d'aplicació del Shelly Plus 1 PM](https://shelly.cloud/documents/user_guide/shelly_plus_1pm_app.pdf).
* [Guia d'usuari del Shelly Plus 1 PM](https://shelly.cloud/documents/user_guide/Shelly_Plus-1PM_multilanguage_v08_web.pdf).

### Thread i Matter
* [Aqara, vídeo promocional](https://youtu.be/6pFn5IwFtmo).
* [Explicació de Thread-Matter feta per Aqara](https://youtu.be/3VI-yzvB4oY).
* [Smart Home Protocols: Thread Explained!](https://youtu.be/0JC4tNe0OS4).
* [Llistat de productes certificats](https://www.threadgroup.org/What-is-Thread/Thread-Benefits#certifiedproducts).
* [Futur ESP32-H2 amb Zigbee-Thread](https://www.espressif.com/en/news/ESP32_H2).

### Simon
* [Vídeo Simon 270](https://youtu.be/JCwgFkpCOdU)
* [Simon webinar z-wave](https://youtu.be/X-xySp9QinI)
* [Catàleg Simon 270](https://resources.simonelectric.com/hubfs/Cat%C3%A1logo%20Simon%20270.pdf)
* [Catàleg Simon 100](https://recursos.detailerssimon.com/hubfs/SIC/Ebooks/Simon%20100/Cat%C3%A1logo/Simon%20-%20Cat%C3%A1logo%20Simon%20100.pdf)
* [Guia aplicaciones Simon 100](https://recursos.detailerssimon.com/hubfs/Guia%20de%20Aplicaciones%20Simon100.pdf)
* [Guia usuario Simon 100](https://recursos.detailerssimon.com/hubfs/Guia%20de%20Usuario%20Simon100.pdf)
* [Catàleg general Simon](https://cdn2.hubspot.net/hubfs/235604/SIC/Ebooks/Simon%20general%202018/Catalogo%20General%20Simon%20N%C2%BA101-2018.pdf)
* [Ebook Simon 100](https://cdn2.hubspot.net/hubfs/235604/SIC/Ebooks/Simon%20general%202018/Catalogo%20General%20Simon%20N%C2%BA101-2018.pdf)
* [Tarifes Simon](https://recursos.detailerssimon.com/hubfs/Tarifa%20General%202022/Simon-T103-ESP-Abril.pdf)

### Valena next with netatmo 
* [Guia tècnica Valena](https://www.legrand.es/documentos/Guia-Tecnica-Valena-%20Next-with-Netatmo-Legrand.pdf).
* [LLista de reproducció de Valena](https://www.youtube.com/playlist?list=PLtbqsvd39xJEsewfYGfC9_cBFSjdv1mYn).
* [CX3 with Netatmo](https://www.netatmo.com/es-es/partners/drivia)

### Tuya
* [Tuya web oficial](https://www.tuya.com/).
* [Endoll intel·ligent Garza](https://garza.es/conectividad/401262-Enchufe_Inteligente_Wifi_-8430624012622.html). [Nanxin](http://nanxin88.com/productView.aspx?view=882&id=109).

### Aqara
* [Aqara web oficial](https://www.aqara.com/en/home.html).
* [Hogar inteligente](https://hogarinteligente.tech/aqara).

### Zigbee
[Repositori dispositius zigbee](https://zigbee.blakadder.com/index.html).

### Home assistant
* [Instal·lar Home assistant](https://programarfacil.com/domotica/home-assistant/)

### Esphome
* [Instal.lar esphome dins de home assistant (En Raspberry Pi 3 no funciona)](https://esphome.io/guides/getting_started_hassio.html#getting-started-with-esphome-and-home-assistant).
* [Instal.lar esphome en windows](https://esphome.io/guides/installing_esphome.html#windows).
* [Iniciar un projecte a ma](https://esphome.io/guides/getting_started_command_line.html#creating-a-project).
#### Exemples de configuracions per una [nodemcu (ESP8266)](https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2019/05/ESP8266-NodeMCU-kit-12-E-pinout-gpio-pin.png?quality=100&strip=all&ssl=1).
* Per afegir multiples wifis:
```
wifi:
  networks:
  - ssid: "IoT3"
    password: "Curs2022#"
  - ssid: "emed"
    password: "pitufito*"

```
* Si fem servir per exemple la GPIO13 per connectar un relé:
``` 
switch:
  - platform: gpio
    name: "Q13"
    id: Q13
    pin: GPIO13
    inverted: false 
 ```
* Si tenim un pulsador a GPIO14 i volem controlar el rele Q13
```
binary_sensor:
  - platform: gpio
    name: "I14"
    pin:
      number: 14
      inverted: false
      mode: input
    on_press:
      then:
        - switch.toggle: Q13   
 ```
 * Si ara dins de la secció **switch** afegeixo:
 ```
 - platform: gpio
    name: "builtin led"
    pin: GPIO16
    inverted: true 
    id: builtin_led  
 ```
 I afageixo això:
 ```
 interval:
  - interval: 2sec
    then:
      - if:
          condition: api.connected
          then:
            - switch.toggle: builtin_led   
            
  ```
  Tindré un led intermitant cada 2 segons indicant "aquí hi ha vida!". 
  * Control per programació horària:
  ```
  time:
  - platform: sntp
    id: sntp_time 
    timezone: Europe/Andorra
    on_time:
      # Cron syntax, trigger every 5 sec
      - cron: '/5 * * * * *'
        then:
          - switch.toggle: Q13
          
     # Every morning on week
      - seconds: 0
        minutes: 51
        hours: 22
        days_of_week: MON-SUN
        then:
          - switch.turn_on: Q13
     # Every morning on week
      - seconds: 0
        minutes: 52
        hours: 22
        days_of_week: MON-SUN
        then:
          - switch.turn_off: Q13    
``` 
  
### OFF TOPIC
* Descarregar W10 LTSC: [LLoc web oficial](https://software-download.microsoft.com/download/sg/444969d5-f34g-4e03-ac9d-1f9786c69161/19044.1288.211006-0501.21h2_release_svc_refresh_CLIENT_LTSC_EVAL_x64FRE_es-es.iso) [.](https://www.tipstecnologicos.com/2021/04/como-activar-windows-10-desde-cmd.html)

* Administrar programes ràpidament amb Chocolatey
    1. Obrir el PowerShell com administrador.
    2. Executar aquests comandaments:
```
Set-ExecutionPolicy AllSigned

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

choco feature enable -n allowGlobalConfirmation

choco install googlechrome firefox office365proplus winrar adobereader 7zip ccleanerportable vlc inkscape gimp
```
* Recordeu que el office 365 plus es una demo.

* Per actualitzar tots els programes alhora:
``
choco upgrade all -y
``
* Per desinstal·lar un programa:
``
choco uninstall nomPrograma -y
``

### DOCKER
* [Instal.lar docker a Debian](https://docs.docker.com/engine/install/debian/#install-using-the-convenience-script).
* Instal.lar Portainer:
```
docker run -d -p 8010:8000 -p 9000:9000 -p 9444:9443 \
    --name=myportainer --restart=always \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v portainer_data:/data \
    portainer/portainer-ce
    
```
* Instal.lar node-red
1. Faig un directory my_docker 
2. Creo subdirectoris per cada node-red, p.ex. `/home/elMeuUsuari/my_docker/nodered00` i `/home/elMeuUsuari/my_docker/nodered01`
3. Permisos: `sudo chown -R 1000:1000 ~/my_docker`
4. Ara fem:
```
docker run -d -p 1880:1880 -v /home/elMeuUsuari/my_docker/nodered00:/data --restart unless-stopped --name mynodered00 nodered/node-red
docker run -d -p 1881:1880 -v /home/elMeuUsuari/my_docker/nodered01:/data --restart unless-stopped --name mynodered01 nodered/node-red
```
5. Actualitzar node-red
```
docker pull nodered/node-red
docker stop mynodered00
docker rm mynodered00
docker run -d -p 1880:1880 -v /home/elMeuUsuari/my_docker/nodered00:/data --restart unless-stopped --name mynodered00 nodered/node-red
```
