# wifi-pineapple-war-driver
Automate your Wifi Pineapple Mk. 7 Workflow!

```                                                                                                                           
                             _      _                        _           
__      ____ _ _ __       __| |_ __(_)_   _____ _ __. ._ __ | |__  _ __  
\ \ /\ / / _` | '__|____ / _` | '__| \ \ / / _ \ '__. | '_ \| '_ \| '_ \ 
 \ V  V / (_| | | |_____| (_| | |  | |\ V /  __/ |_   | |_) | | | | |_) |
  \_/\_/ \__,_|_|        \__,_|_|  |_| \_/ \___|_(_)  | .__/|_| |_| .__/ 
                                                      |_|         |_|    
                                                                               
 ```                                                                                                                                                                                                                                       

This simple PHP script is an aggressive war-driver for the [Hak Wifi Pineapple Mark VII](https://shop.hak5.org/products/wifi-pineapple) to fully automate your recon, 
de-authing and handshake capturing.  Turn this thing on, take your Pineapple for a walk around town, and collect those handshakes without any effort.

Pair this with [loot-n-scoot.sh](https://github.com/sailboat-anon/wifi-pineapple-mark-vii) to auto-submit your captures to onlinehashcrack.com for free, 
hands-off cracking.  Just run it on a cron and check your inbox :)

Requirements:
```
php-cli
```

Use:
```
Run on your local machine, not the Wifi Pineapple (better performance)
- git clone git://github.com/sailboat-anon/wifi-pineapple-war-driver.git
- nano war-driver.php
- Modify $config to match the server, port, username, password for your Wifi Pineapple. 
- php war-driver.php
```

Workflow:
```
- set pineAP settings to AGGRESSIVE, broadcasting, allowing connections, auto-restart, etc
- run recon for 90 seconds, identify all APs with associated clients
- start handshake capture
- de-auth all clients related to AP, repeat 20 seconds later; total 2 mins
- handshakes captured, available for use
- repeat: move to next AP with associated clients, de-auth, etc.
```


```
                  .
                .'|     .8
               .  |    .8:
              .   |   .8;:        .8
             .    |  .8;;:    |  .8;
            .     n .8;;;:    | .8;;;
           .      M.8;;;;;:   |,8;;;;;
          .    .,"n8;;;;;;:   |8;;;;;;
         .   .',  n;;;;;;;:   M;;;;;;;;
        .  ,' ,   n;;;;;;;;:  n;;;;;;;;;
       . ,'  ,    N;;;;;;;;:  n;;;;;;;;;
      . '   ,     N;;;;;;;;;: N;;;;;;;;;;
     .,'   .      N;;;;;;;;;: N;;;;;;;;;;
    ..    ,       N6666666666 N6666666666
    I    ,        M           M
   ---nnnnn_______M___________M______mmnnn
         "-.                          /
  __________"-_______________________/_________
  ```

![successful_cap](https://github.com/sailboat-anon/wifi-pineapple-war-driver/blob/master/img/success-cap.png)

![successful_run](https://github.com/sailboat-anon/wifi-pineapple-mark-vii/blob/main/img/successful%20run.png)

![submitted_view_ui](https://github.com/sailboat-anon/wifi-pineapple-mark-vii/blob/main/img/submitted-caps.png)
