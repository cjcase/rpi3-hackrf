```
             _ ____        _                _          __ 
         (( (_)___ \      | |              | |        / _|
  _ __ _ __  _  __) |_____| |__   __ _  ___| | ___ __| |_ 
 | '__| '_ \| ||__ <______| '_ \ / _` |/ __| |/ / '__|  _|
 | |  | |_) | |___) |     | | | | (_| | (__|   <| |  | |  
 |_|  | .__/|_|____/      |_| |_|\__,_|\___|_|\_\_|  |_|  
      | |2018.07                                   (( | ))         
      |_|    

```
A remix of Arch Linux ARM for Raspberry Pi 3 B+ built for HackRF and RTL-SDR.  
Here you will find a working Arch Linux image with the latest firmware, drivers and software to use HackRF and RTL-SDR in a Raspberry Pi 3 B+.  

# Installation
 * Grab the latest release
 
 `wget https://<release link here>/rpi3-hackrf.img.tgz`
 
 * unpack and dd image to a micro SD card
 
 `dd if=rpi3-hackrf.img of=/dev/mmcblk0 bs=512k`
  
 * boot into the OS
 * use SSH or connect to a screen/keyboard/mouse and login with default password
 
 ``` 
 Login:    hackrf
 Password: hackrf
 ```
 * Follow the first setup instructions
 * Run the X server  
 `startx`
 * ???
 * PROFIT!
 
  # What's Inside?
 Please check the `packages.txt` file for a full list of the installed software for this distribution. 
 * [Built on PINN for easy recovery/reinstall](https://github.com/procount/pinn)
 * Automagically DHCP connect through eth0 on boot
 * SSH Server listening in port 22
 * First run script for security purpouses (no IoT botnets here, unless you never ran the script)
 * VNC server ready
 * Lightweight but riced desktop LXDE
 * Firefox for your googling/stackoverflow needs
 * GNU Radio
 * GNU Radio Companion
 * gqrx
 
 # Details
 The distro is based on PINNS (a fork of NOOBS) and Arch ARM for rpi arm7, with extra packages for SDR.
 This image was made as light as possible without leaving user friendliness behind. Still the best way to use your rpi3b+ with HackRF is through the command line, feel free to use the graphical interface for tools like GNU Radio Companion, but you can only make your pi go as far as its hardware, it still chokes on audio sampling.  
 
 # How do I run HackRF in my Arch Linux install?
 The juice in your Raspberry Pi 3 B+ is not enough for your SDR needs? Worry not! Making the HackRF chooch on your Arch Linux laptop is as easy as 1,2,3.  
 ```
 pacman -Syu gnuradio-companion gnuradio-osmosdr hackrf pulseaudio gqrx
 ```
 
 # Issues & Pull Requests 
 I imagine the image is far from perfect, if you find a bug or would like me to add new software/drivers/features please do let me know through issues.
 Pull requests for improvements are greatly accepted.
 
 `made with <3 for fellow hackers`
