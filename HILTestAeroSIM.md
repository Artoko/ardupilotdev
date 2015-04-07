# Introduction #

Here you will find a good and cheap method to test yourself  the [ArduCopter](http://code.google.com/p/arducopter/) firmware in HIL (Hardware In the Loop) mode with the [AeroSIM-RC simulator](http://www.aerosimrc.com/j/index.php/en).

![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_sim.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_sim.jpg)

## Details ##
**Hardware requirement:**
  * a PC computer,
  * an ArduMega board APMv1 (1280, 2560)or APMv2,for the APMv1, no IMU shield is required (more info [HERE](http://code.google.com/p/ardupilot-mega/)),
  * the [AeroSIM-RC v3.81](http://www.aerosimrc.com/j/index.php/en/downloads) simulator (Demo or Retail version):
  * update the Aerosim-RC 3.81 to the v3.83 by downloading this update:  http://www.aerosimrc.com/downloads/AeroSIMRC_3.83-3.81.exe
  * the firmware [ArduCopter v2.4.1xp2 DCM](http://ardupilotdev.googlecode.com/files/ArduCopter_241xp2_DCM.zip) or more installed on the APM,
  * the [Mission Planner v1.1.48](http://code.google.com/p/ardupilot-mega/downloads/list) (or more) installed on the PC, you may download the latest version in the [Ardupilot-mega official repository](http://code.google.com/p/ardupilot-mega/source/browse/) with GIT
  * the [HIL setups and param files](http://ardupilotdev.googlecode.com/files/ArduCopter_HIL_setups.zip) for the HIL simulation
  * You will find in the [ArduCopter\_HIL\_setups.zip](http://ardupilotdev.googlecode.com/files/ArduCopter_HIL_setups.zip), , the AeroSim plug-in (plugin\_AeroSIMRC.dll) in the AeroSIM\_HIL/APMHil/ folder.
  * You will find also in the [ArduCopter\_HIL\_setups.zip](http://ardupilotdev.googlecode.com/files/ArduCopter_HIL_setups.zip), the quadcopter model MD4.mdl in the AeroSIM\_HIL/ folder.

## Installation ##

  * Unzip the archive ArduCopter\_HIL\_setups.zip
  * copy the folder \APMHill in the AeroSiM folder c:\Program Files (x86)\Plugin\
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_plugin.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_plugin.jpg)
  * copy the quadcopter model MD4.mdl in the AeroSiM folder c:\Program Files (x86)\Data\
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_model1.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_model1.jpg)
  * check that in the firmware the parameters of the APM\_Config.h are set, then upload the firmware to the APM:

```
  #define HIL_MODE 	HIL_MODE_ATTITUDE
  #define X_PLANE 	ENABLED
```
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_uploadl.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_uploadl.jpg)

  * upload the AC241xp2\_MD4\_HIL.param (found in the ArduCopter\_HIL\_setups\AeroSim\_Hill folder ) with the mission planner to your APM board.
![http://ardupilotdev.googlecode.com/svn/images/MD4_PID.jpg](http://ardupilotdev.googlecode.com/svn/images/MD4_PID.jpg)

## Testing ##

  * launch the APM mission planner
  * click on the Tab **simulation**
  * click on **CONNECT** on the top right corner
  * click on the button **AeroSim** and set the parameters as below:
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_setup.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_setup.jpg)
  * click on the Tab **Configuration**, do the stick calibration
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_calib.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_calib.jpg)
  * click on the Tab **Mode**, set the MODE
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_Mode.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_Mode.jpg)
  * click again on the Tab **simulation**
  * click on **Start simulation**
  * launch the **AeroSIM-RC** then select **Plugin** and **APMHil**
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_plugin_select.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_plugin_select.jpg)
  * select the model **MD4**
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_model.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_model.jpg)

Enjoy flying with AeroSIM in HIL mode
![http://ardupilotdev.googlecode.com/svn/images/AeroSIM_sim.jpg](http://ardupilotdev.googlecode.com/svn/images/AeroSIM_sim.jpg)

You will find some videos of HIL simulations at:

http://vimeo.com/37896642

http://vimeo.com/37243083

More infos at:
http://diydrones.com/profile/JeanLouisNaudin

Enjoy with the HIL simulation with **AeroSIM-RC**...

Regards,
Jean-Louis