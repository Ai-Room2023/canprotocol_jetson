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

add a line

```
spidev

```
Press ctrl+x and then press Y, press Enter to save and exit, and then open the hardware SPI:

```
sudo /opt/nvidia/jetson-io/jetson-io.py

```

as shown
Choose to configure 40PIN pin
Use the keyboard to select, configure the pins

![1 1](https://github.com/Ai-Room2023/canprotocol_jetson/assets/140303548/6351ff88-0b76-4fed-96f9-1b7eaf52ee35)

Use the keyboard to select， move to SPI1 and press Enter to confirm

![1 2](https://github.com/Ai-Room2023/canprotocol_jetson/assets/140303548/55cb1453-8ba2-4657-9fdf-755ed3f9a4e8)

Save and select restart (keep Enter to restart)

![1 3](https://github.com/Ai-Room2023/canprotocol_jetson/assets/140303548/aa32aefe-ecbc-41fb-9847-750988a4c816)

After restarting, ls /dev/spidev* can see the device number

![1 4](https://github.com/Ai-Room2023/canprotocol_jetson/assets/140303548/6bb60982-2e0f-4f0b-aee2-b19a5adb1dd3)

<h3> CAN Test </h3>

Please connect the hardware first, and then run the program. As SPI to CAN and the default crystal oscillator is 8M, the temporary baud rate is 500Kbps.
The Python driver provided by this product currently supports a baud rate of 500Kbps (the default is 500Kbps), pay attention to select the baud rate of the other end of the communication:

```
cd RS485_CAN_for_JetsonNano_Code
sudo python cantest.py

```
