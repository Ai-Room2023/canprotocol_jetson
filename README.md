# canprotocol_jetson
Using can protocol in Jetson Nano with waveshare jetson nano can shield

![141](https://github.com/Ai-Room2023/canprotocol_jetson/assets/140303548/7fed9a9a-642f-472e-955d-1d159e406466)

<h2> HOW TO USE </h2> 

<h3> install library </h3>
```

sudo apt-get install minicom 
sudo apt-get install python-pip nano
sudo pip install pyserial
sudo pip install spidev==3.1
```


<h3> enable SPI </h3>
After executing the above, add in the following file:
```
sudo nano /etc/modules-load.d/modules.conf
```
