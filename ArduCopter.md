# Introduction #

Here you will find a good and cheap method to test yourself  the [ArduCopter](http://code.google.com/p/arducopter/) firmware in HIL (Hardware In the Loop) mode with the [X-Plane simulator](http://www.x-plane.com).

![http://ardupilotdev.googlecode.com/svn/images/hilloiter1.png](http://ardupilotdev.googlecode.com/svn/images/hilloiter1.png)
![http://ardupilotdev.googlecode.com/svn/images/hilloiter2.png](http://ardupilotdev.googlecode.com/svn/images/hilloiter2.png)

## Details ##
**Hardware requirement:**
  * a PC computer,
  * an ArduMega board APMv1 (1280, 2560)or APMv2,for the APMv1, no IMU shield is required (more info [HERE](http://code.google.com/p/ardupilot-mega/)),
  * the [X-Plane v9.70](http://www.x-plane.com/downloads/older/) simulator (Demo or Retail version),
  * the firmware [ArduCopter v2.1.1 R6](http://ardupilotdev.googlecode.com/files/ArduCopter_2_1_1r6.zip) or more installed on the APM,
  * the [Mission Planner v1.1.18](http://code.google.com/p/ardupilot-mega/downloads/list) (or more) installed on the PC, you may download the latest version in the [Ardupilot-mega official repository](http://code.google.com/p/ardupilot-mega/source/browse/) with GIT
  * the [Starter Pack](http://ardupilotdev.googlecode.com/files/starter_pack.zip) for the HIL simulation

![http://ardupilotdev.googlecode.com/svn/images/arducopterHil1.jpg](http://ardupilotdev.googlecode.com/svn/images/arducopterHil1.jpg)

## Installation ##

The X-Plane v9.70 and Mission Planner must be installed on the PC and and the ArduCopter firmware installed in the APM board.

You need to add some additional files to run the full ArduCopter simulation in HIL mode, you will find [the started package HERE](http://ardupilotdev.googlecode.com/files/starter_pack.zip)

  * copy the folder **QRO\_X** into the folder **X-Plane 9 Demo/Aicraft/Radio Control/**  this is the quadcopter model for X-Plane
  * copy the file **LOWI\_AIRPORT.sit** in the folder **X-Plane 9 Demo/Output/situations/** this is the situation for the simulation
  * upload the param file **AC211r6\_Xplane.param** with the APM Planner to the APM board
  * upload the mission file **LOWI\_AIRPORT\_MISSION.txt** with the APM Planner to the APM board

Launch the X-plane simulator, when X-plane is ready, you need to set the correct parameters for the network connection (see below):

![http://ardupilotdev.googlecode.com/svn/images/XplaneV970set1.jpg](http://ardupilotdev.googlecode.com/svn/images/XplaneV970set1.jpg)
![http://ardupilotdev.googlecode.com/svn/images/XplaneV970set2.jpg](http://ardupilotdev.googlecode.com/svn/images/XplaneV970set2.jpg)

## Testing ##

The mission file that you have uploaded is a demo of a full autonomous mission done at the LOWI airport (the airport set by default in the X-Plane demo version).
You will find a full video of this flight [HERE](http://vimeo.com/34606524)
How to start the test mission:
  1. Launch and connect the APM Planner to the ArduMega board
  1. click on the Simulation Tab then click on "Start Xplane", if not yet launched
  1. On **X-Plane** file/load the situation **LOWI\_AIRPORT.sit**
  1. then select the chase view (A)
  1. On the APM planner, click to **Start the Simulation**, see below:
![http://ardupilotdev.googlecode.com/svn/images/startsim.jpg](http://ardupilotdev.googlecode.com/svn/images/startsim.jpg)
  1. With the Notepad open the file **scriptAPMlowi.txt**, this the script for running the mission, you may of course use your transmitter if you have connected a receiver to the APM board.
  1. select all the script then Copy it into the clipboard (Ctrl-C)
  1. On the APM planner, click on the tab 'Flight Data', then click on the button 'Script' at the bottom left,
  1. then Paste (Ctrl-V) the clipboard to the script windows
  1. close the script windows and click OK to run the script...

![http://ardupilotdev.googlecode.com/svn/images/Launch_script.jpg](http://ardupilotdev.googlecode.com/svn/images/Launch_script.jpg)

If all is ok, you will see the quadcopter flying in a full autonomous flight...

More infos at:
http://diydrones.com/profiles/blogs/arducopter-in-action-testing-the-quadcopter-hil-mode-on-x-plane

Enjoy with the HIL simulation...

Regards,
Jean-Louis