![Logo](admin/broadlink.png)
ioBroker.broadlink  
==================

---

# NOT MAINTAINED ANYMORE

**This project is not maintained anymore, because personal reasons. Please use: 
https://github.com/frankjoke/ioBroker.broadlink2**

---

![Number of Installations](http://iobroker.live/badges/broadlink-installed.svg) ![Number of Installations](http://iobroker.live/badges/broadlink-stable.svg) [![NPM version](http://img.shields.io/npm/v/iobroker.broadlink.svg)](https://www.npmjs.com/package/iobroker.broadlink)
[![Downloads](https://img.shields.io/npm/dm/iobroker.broadlink.svg)](https://www.npmjs.com/package/iobroker.broadlink)

[![NPM](https://nodei.co/npm/iobroker.broadlink.png?downloads=true)](https://nodei.co/npm/iobroker.broadlink/)

**Tests:** Linux/Mac: [![Travis-CI Build Status](https://travis-ci.org/hieblmedia/ioBroker.broadlink.svg?branch=master)](https://travis-ci.org/hieblmedia/ioBroker.broadlink)
Windows: [![AppVeyor Build status](https://ci.appveyor.com/api/projects/status/pil6266rrtw6l5c0?svg=true)](https://ci.appveyor.com/project/hieblmedia/iobroker-broadlink)
**This adapter needs at least Node 4.x**

#### Installation
Execute the following command in the iobroker directory (e.g. /opt/iobroker)  
```
# cd /opt/iobroker
# npm install iobroker.broadlink
# iobroker upload broadlink
```

This is an ioBroker adapter for Broadlink RM3 Mini/RM3 Pro to learn and send signals.

## Configuration
Enter the IP address in the configuration

## How-To learn codes
* In Objects of ioBroker you can find "broadlink.[n].enableLearningMode".
* Set this object to true. (e.g. on RM3 mini or Pro the LED is light up)
* Now press some button on your remote control within 30 seconds.
* An new Object should now appear within the Object "broadlink.[n].learnedSignals" with the name ">>> Learned, please describe"

It is also possible to use the codes from [RM-Bridge](http://rm-bridge.fun2code.de/).  
You just need to prepend "CODE_".

## How-To structure codes outside learnedSignals
* You can create your state object everywhere in the instance to build your own channel and device structure.
* All you need is the CODE_[n] from learnedSignals
* You can use the signal code (CODE_12345...) as object id or in name. Depends on what you prefer.

![Simple object structure example](doc/structure_example.png)

## Known-Issues
If you learn the same signal multiple times the code can be different everytime. This can not be changed.
