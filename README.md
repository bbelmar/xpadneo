This is the DKMS version of my hid-xpadneo driver. Take a look in the master branch for further information.

## Prerequisites
Make sure you have installed the following packages
* dkms
* linux-headers
* build-essential / base-devel 

## Installation
* Download the Repository to your local machine  
  `git clone https://github.com/atar-axis/xpadneo.git -b dkms`
* Copy the `hid-xpadneo-<version>` folder into the `/usr/src/` directory (alternatively, create a softlink)  
  `sudo ln -s ~/xpadneo/hid-xpadneo-0.2.0/ /usr/src/`
* Add the driver to DKMS and install it
  * `sudo dkms add hid-xpadneo -v <version>`
  * `sudo dkms install hid-xpadneo -v <version>`
  
## Connect
* `sudo bluetoothctl`
* `scan on`
* push the connect button on upper side of the gamepad until the light starts flashing fast
* wait for the gamepad to show up 
* `pair <MAC>`
* `trust <MAC>`
* `connect <MAC>`

You know that everything works fine when you feel the gamepad rumbling ;)

