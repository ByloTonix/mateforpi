<h1 align="center">MateForPi</h1>

![alt text](https://github.com/ByloTonix/mateforpi/blob/main/screenshot1.png)
MateForPi is a simple script for installing a fully working MATE environment on Raspberry Pi OS.

Before running the script, you need to perform some actions:
- Install Raspberry Pi OS Lite (not tested on the 64-bit version, but it works) and connect the board via Ethernet (preferably) or Wi-Fi.
- If you have not used Raspberry Pi Imager to flash an image and create your own user, then
  - Enter default login data (login/password): pi/raspberry
  - Create a new user and delete a standard one:
    - ``sh sudo adduser your_name ``
    - ``sh sudo adduser your_name sudo ``
    - Create the file using ``sh sudo visudo /etc/sudoers.d/010_YOURNICKNAME-nopasswd ``
    - Insert the following contents on a single line: ``sh YOURNICKNAME ALL=(ALL) NOPASSWD: ALL``
    - Save the file and exit.
  - login with your new account created and ``sh sudo userdel -r pi ``

- Open the configuration menu:
```sh
sudo raspi-config
```
- In the "Performance Options" section, you can select "GPU Memory" and enter the prefered value in the input field, i.e. "320". If you use Raspberry Pi 4 and want to overclock your board, then open the configuration file:
```sh
sudo nano /boot/config.txt
```
and enter at the end of the file:

```sh
#for RPi 4
over_voltage=6
arm_freq=2000
gpu_freq=750
```

How we are ready to start installation:
```sh
sudo apt install git --no-install-recommends && git clone https://github.com/ByloTonix/mateforpi/ && cd mateforpi && sudo bash mateforpi
```

My MATE Desktop after 3-min customization:

![alt text](https://github.com/ByloTonix/mateforpi/blob/main/screenshot2.png)

### Important Info:
- Since Raspberry Pi OS Bookworm and Raspberry Pi 5 were released, this guide can be outdated.
