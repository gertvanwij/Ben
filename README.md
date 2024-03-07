# Ben
informatie

![image](https://github.com/gertvanwij/Ben/assets/65614247/4e85d320-313a-4784-b3bc-09ff509c4aef)


{% if is_state('switch.sproeiers_gras', 'on') or
       is_state('switch.sproeiers_noord', 'on') or
       is_state('switch.sproeiers_oost', 'on') or
       is_state('switch.sproeiers_zuid', 'on')%}
         green
       {% else %}
         orange
       {% endif %} 


Dailey sensor

https://github.com/jeroenterheerdt/HADailySensor
