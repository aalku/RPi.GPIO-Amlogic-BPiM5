
# RPi.GPIO-Amlogic  
  
RPi.GPIO port with support for Bananapi M5/M2Pro/M2S/CM4  

Fork by aalku to support Banana Pi M5 on Armbian 23, kernel 6.x.

## Based on:  
  
RPi.GPIO by Ben Croston  
  https://sourceforge.net/projects/raspberry-gpio-python/  

Bananapi M5/M2Pro/M2S/CM4 WiringPi port  
  https://github.com/Dangku/amlogic-wiringPi  

awesometic's Odroid RPi.GPIO port  
  https://github.com/awesometic/RPi.GPIO-Odroid  

Upstream repository by Dangku
  https://github.com/Dangku/RPi.GPIO-Amlogic
  
  
## License  
RPi.GPIO is distributed under MIT license, but wiringPi uses LGPL 3.  Since this project  
contains code from both projects, it is licensed under the slightly more restrictive LGPL v3.  
  
  
## Status  
Working for simple IO on Bananapi M5/M2Pro/M2S/CM4  
PWM, events, analog read, ... not implemented  
  
  
## Building  
1) Install build-essential, python, python-dev, python-setuptools, git  
2) git clone https://github.com/aalku/RPi.GPIO-Amlogic-BPiM5.git
3) cd RPi.GPIO-Amlogic  
4) sudo python setup.py clean --all  
5) sudo python setup.py build install  

## Notes  
Apps require root (eg 'sudo python testapp.py')  
When using BCM mode, RPi BCM numbers are passed to GPIO.xxx and translated internally to Amlogic GPIO numbers  
Compare RPi connector pinout / BCM chart and Amlogic pinout to match RPi BCM with Amlogic pins  
