_This project is going to read PH, Temperature and Dissolved Oxygen (DO) from sensors and write them to a database_ 

This project uses a Raspberry PI 3b, a Whitebox carrier boards for the Raspberry Pi platform  and Atlas Scientific EZO sensors and probes.
All the parts are available from https://atlas-scientific.com/

Full hardware documentation, quickstart guide for the Whitebox Tentacle T3 for Raspberry Pi can be found here https://www.whiteboxes.ch/docs/tentacle/t3

# Preparing the Raspberry Pi #
### Install the latest Raspberry Pi OS
Follow the instructions on this page to get Raspberry Pi OS running
https://www.raspberrypi.org/downloads/raspberry-pi-os/

# Download code.
    
    cd ~
    git clone https://github.com/graber65/ezo-sensors.git


# I2C MODE #

### Enable I2C bus on the Raspberry Pi ###

Enable I2C bus on the Raspberry Pi by following this:

https://learn.adafruit.com/adafruits-raspberry-pi-lesson-4-gpio-setup/configuring-i2c

### Enable I2C mode on the EZO chips ###

By default, the EZO are configured for uart, to work with the Whitebox carrier boards they must be set to I2C mode.

refer to the data sheets for each sensor on how to wire them up on a breadboard to switch them over, or get an I2C toggler from https://atlas-scientific.com/ezo-accessories/i2c-toggler/ 



You can confirm that the setup worked and sensors are present with the `sudo i2cdetect -y 1` command.
