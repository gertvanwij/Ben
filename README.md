# Ben
informatie

sensor windrichting

in de file sensor.yaml een nieuwe sensor maken volgens 
![image](https://github.com/user-attachments/assets/9b8c0fd4-d18b-43cc-a218-eb66c9763f8f)

LET OP!
waarschijnkijk staat er al helemaal boven aan in sensor.yaml

- platform: template
  sensors:

dan alleen dit gebruiken

    windnaam:
      value_template: >
        {% set direction = ['N','NNE','NE','ENE','E','ESE','SE','SSE','S','SSW','SW','WSW','W','WNW','NW','NNW','N'] %}
        {% set degree = states('sensor.windrichting_azimut')|float %}
        {{ direction[((degree+11.25)/22.5)|int] }}

deze sensor (windnaam) dan gebruiken in de windroos

=============================================================================================================================================



![image](https://github.com/gertvanwij/Ben/assets/65614247/4e85d320-313a-4784-b3bc-09ff509c4aef)


{% if is_state('switch.sproeiers_gras', 'on') or
       is_state('switch.sproeiers_noord', 'on') or
       is_state('switch.sproeiers_oost', 'on') or
       is_state('switch.sproeiers_zuid', 'on')%}
         green
       {% else %}
         orange
       {% endif %} 
=============================================================================================================================================================

Dailey sensor

https://github.com/jeroenterheerdt/HADailySensor

=============================================================================================================================================================




https://github.com/bigbeartechworld/big-bear-video-assets/tree/main/how-to-install-frigate-on-casa-os



Vaatwasser is klaar  blueprint

https://community.home-assistant.io/t/notify-or-do-something-when-an-appliance-like-a-dishwasher-or-washing-machine-finishes/254841

=============================================================================================================================================================


rtsp://testuser:foscam@192.168.1.11:88/videoMain  

rtsp://admin:admin@192.168.1.20:150/videoMain 

https://www.ispyconnect.com/camera/foscam

https://docs.frigate.video/configuration/camera_specific/#mjpeg-cameras
========================================================================================================================
/dev/sdb2: UUID="62964b68-f460-42c8-ad58-f1bf74ddad22" BLOCK_SIZE="4096" TYPE="ext4" PARTUUID="f1218d67-02"



3 uur goedkope stroom
https://www.creatingsmarthome.com/index.php/2023/04/12/home-assistant-advanced-nord-pool-cheapest-hours-with-local-calendar-support/?fbclid=IwY2xjawD0TKVleHRuA2FlbQIxMQABHfXD4-cueghA4V--F-4DIrtGfTY4YxfzsBblfJ8ODgcdZyM7vnV6kXtbzQ_aem_L4Ex7xpMrNqzHWsV9OzQhg&sfnsn=mo
/mnt/camera/frigate


===============================================================================================================================
https://community.bigbeartechworld.com/t/how-to-migrate-casaos-data-to-a-new-drive-and-mount-it-permanently/217
