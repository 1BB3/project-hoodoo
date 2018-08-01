# project-hoodoo
Control your Android from Linux...
_Only tested in Xiaomi Redminote4 (mido) (MIUI 10)_

## Instructions
1. Enable ADB debugging in your android, and connect it to your linux and authorize it.
2. If you want to control it over network, then you need to open tcp port for ADB debugging service.

    For this you need to root your android and run the following command in a terminal.
    ```$ su
       $ setprop service.adb.tcp.port 7091
       $ stop adbd
       $ start adbd
    ```
    You can change `7091` and set your custom port.
    If you want to revert to USB port then change the port to `-1`.
    ```$ su
       $ setprop service.adb.tcp.port -1
       $ stop adbd
       $ start adbd
    ```
    _When connecting later don't forget to authorize your linux._
3. After setting up your android, to install mido run the `install.sh` script. 
    
    You can run it from the current directory.
    ```
    $ ./install.sh
    ```
    
## Commands
1. configure
    
    --ip XXX.XXX.XXX.XXX
    
    --port XXXX
    
    --adb-connection \[tcp/usb\]
    
    --device-pin XXXX
    
    --unlock-swipe-direction \[up/down/left/right\]
    
2. config
3. connect
4. wake
5. sleep / lock

    --close-all
    
6. unlock
7. 2cars
8. recent

    --clear
    
9. home
10. back
11. vol+ \[2,3,4...\]
12. vol- \[2,3,4...\]
13. play
14. pause
15. next
16. previous / prev
17. search

    --google

_...More to come..._

