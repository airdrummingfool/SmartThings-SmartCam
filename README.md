# Samsung SmartCam Motion Detection Switch
This open-source software is free to use and enjoy at no cost to you. If you would like to thank the developer (me!) please consider donating.

[![PayPal.me](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://paypal.me/TommyGoode) (or [Square Cash](https://cash.me/$TommyG)) 


## Description
This code allows SmartThings to toggle the motion detection setting on a supported Samsung SmartCam. Combined with a SmartApp such as `Smart Lights` (under "Lights and Switches") or `CoRE`, a SmartCam can have its motion detection enabled when Smart Home Monitor is armed, and disabled when SHM is disarmed.

The device handler takes care of the required Digest authentication for communication with the camera. Once you've entered the device IP and password in settings, no extra steps are required to authenticate.


### Compatibility
This device handler has been tested on the following models/firmware versions. If you use it with a different setup, please let me know and I'll update this list.

* SNH-P6410BN (`1.08_160629`)


## Installation
Note: The camera must be installed and connected to your local network before proceeding. It does *not* need to be set up in SmartThings (this process will not integrate the camera with SmartThings).

**The SmartCam must have a static IP.**

### 1. Install the Device Handler

#### Using Github integration (recommended)
1. In the SmartThings IDE, click "My Device Handlers"
1. Click "Settings"
1. Click "Add new repository" and fill in the following details
   * Owner: `airdrummingfool`
   * Name: `SmartThings-SmartCam`
   * Branch: `airdrummingfool`
1. Click "Save"
1. Back on the Device Handlers page, click "Update From Repo" to open the repo list
1. Find "SmartCam-Motion-Detection-Switch (master)" in the list and click it
1. Check the box next to `devicetypes/airdrummingfool/smartcam-motion-detection.src/smartcam-motion-detection.groovy`
1. Check `Publish` at the bottom, and then "Execute Update"


#### Manual installation
1. In the SmartThings IDE, click "My Device Handlers"
1. Click "+ Create New Device Handler"
1. Click the "From Code" tab
1. Paste the Device Handler code into the text field
1. Click "Create"
1. Click "Publish" and "For Me"


### 2. Add a new Device
1. In the SmartThings IDE, click "My Devices" and then "+ New Device".
1. Enter a name and a unique Device Network Id (This can be anything. Do **not** use hex MAC address if you want to use the native SmartThings-SmartCam integration.)
1. Under `Type`, choose **SmartCam Motion Detection Switch**
1. Make sure you set the `Location` and `Hub` appropriately.
1. Click "Create"


### 3. Configure the Device
1. In the mobile app, find your newly-created device (the tile should say "check configuration")
1. Click the cog to go to Device Settings
1. Enter the SmartCam's IP address and password
1. Click "Done" to save

If everything went smoothly, the device tile should be updated to the status of the motion detector (on/off). If not, please double-check the IP address and password and try a "Refresh". If things still don't work, please create an issue on Github or contact me via the SmartThings Community forum. Please include log excerpts!
