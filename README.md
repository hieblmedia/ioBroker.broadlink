![Logo](admin/broadlink.png)
# ioBroker.broadlink
=================

#### Description

Adapter for Broadlink IR  
**[only tested with RM3 Mini atm.]**

**This adapter needs at least Node 4.x**

#### Installation
Execute the following command in the iobroker directory (e.g. /opt/iobroker)  
```
# cd /opt/iobroker
# npm install iobroker.broadlink
# iobroker upload broadlink
```

Or simply install with the GitHub-Url via ioBroker Admin.

#### Configuration
Enter the IP address in the configuration (auto-discover list is possible but not implemented yet)

#### How-To learn IR-Signals
* In Objects of ioBroker you can find "broadlink.[n].enableLearningMode".
* Set this object to true. (e.g. on RM3 mini the LED is light up)
* Now press some button on your remote control within 30 seconds.
* An new Object should now appear within the Object "broadlink.[n].IR_Signals" with the name ">>> Learned, please describe"

#### Known-Issues
If you learn the same code multiple times IR code appears multiple times, because it has some random characters if the buffer is converted to HEX.
Any suggestions to make this consistent are welcome.
