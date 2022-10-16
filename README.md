# custom-cdn
custom cdn


## Start the stack with docker compose

```bash
$ docker-compose up
```

## Stack

1. 5 caching apps with access to the same resources in 'www' folder:

URL - http://localhost:81/images/Xbox4.png

URL - http://localhost:82/images/Xbox4.png

URL - http://localhost:83/images/Xbox4.png

URL - http://localhost:84/images/Xbox4.png

URL - http://localhost:85/images/Xbox4.png


2. 2 Round robin balancers:

URL - http://localhost:800/images/Xbox4.png

URL - http://localhost:900/images/Xbox4.png


3. Updated https://github.com/sulemanhasib43/nginx_1.16.0_geolite2 as geodns:

URL - http://localhost:90/images/Xbox4.png


By default, IP from Poland redirects to loadbalancer1, all other redirects to loadbalander2.
Response header 'custom' shows information about which app responds, 'iso' shows which location you have.

![image](https://user-images.githubusercontent.com/112312750/196042388-5b07e173-8a66-44db-830e-e952497cab3f.png)






