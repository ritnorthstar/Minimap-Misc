Minimap Information
============

#Client

Package Contents

* Nexus 7 tablet
* USB cable
* USB wall adapter
* 4 white-labeled Stick-N-Find beacons (#1-#4)
* 4 yellow-labeled Stick-N-Find beacons (#5-#8) (Property of John Paul Mardelli)


##Requirements

Ensure that the Minimap application is installed, Wi-Fi is connected, and Bluetooth is turned on.  Wi-Fi and Bluetooth can be configured in their respective settings menus by swiping down from the top right portion of the menu bar on the Android home screen.


##Performance

This system was tested in a live demo for attendees at the RIT SE Project Poster Presentation event.  The system performed within a 12 ft x 15 ft space using six beacons.  The user location took about 10-20 seconds to catch up whenever the device was moved with a precision that appeared to be on average within at least 5 ft of the actual device location.  The proximity zone feature took about 5-10 seconds in order to indicate which beacon the device was near while moving between different beacons.  Please note that these are rough estimations of the system performance during this event.

It can be concluded that the proximity zone feature responds more quickly than the indoor positioning feature and can be on average demonstrated with more success.

For best results, move the device from beacon to beacon and look for each beacon corresponding to change color in the map.  For more help, see the Proximity Zones section below.

##Recommended and Default Configurations

There are two recommended setup configurations to achieve the best demonstrability:
Eight beacons placed evenly along the border of a square measuring 25 ft x 25 ft but no larger than 50 ft x 50 ft
Eight beacons placed evenly along the border of a rectangle measuring 12 ft x 36 ft but no larger than 20 ft x 60 ft

In the event of a server or Internet connection failure, the Minimap app is preloaded with a default test map in a setup configuration with eight beacons placed evenly along the border of a 25 ft x 25 ft square.  The beacons are arranged 1 through 8 in increasing order traveling clockwise along the border starting with beacon #1 in the top left corner and finishing with beacon #8 at the midpoint of the left side.  (1, 3, 5, 7 are at corners and 2, 4, 6, 8 are at side midpoints).

This default test configuration can be accessed by selecting the Launch Test Map option in the top right corner of the menu action bar on the application home screen

##Calibration

Minimap uses a default calibration setting that works well in most beacon setups.  If the estimated distances appear to be imprecise by a substantial distance, each beacon can be individually calibrated using the following method for best results:

Stand in the most central location respective to all beacons
Stay in this position for 10-20 seconds to allow RSSI readings to be gathered from all beacons
Press and hold on the screen at the point that best represents your actual location with respect to the other beacons.
A short message should appear on screen verifying that the calibration was successful

The calibration can be restored to its original setting by selecting Reset calibration under the options menu in the top right corner of the menu action bar when viewing the map.

##Proximity Zones

Beacons will appear yellow when the Android device is within a certain minimum distance to the beacon, i.e. within that beacon’s proximity zone.  This minimum distance can be modified from its default value of 3 feet under Proximity Zone Range in the Settings menu in the top right corner of the menu action bar when viewing the map.

This feature can also be disabled under the Enabled proximity zones option in the Settings menu.


##Troubleshooting Bluetooth

A signal from at least four Bluetooth beacons is required to triangulate a position.  You can verify that a signal has been received by a beacon when a blue circle indicating the range to that beacon is drawn around that beacon.  This graphical indication can be disabled under the Show beacon range circles in the Settings menu.

If the device fails to receive signal strength readings after 15-30 seconds, the Bluetooth adapter might need to be restarted.  Select the Restart bluetooth option under the options menu in the top right corner of the action menu bar.

If the device still fails to receive signal strength readings after 15-30 seconds, the device will need to be rebooted in order to return the Bluetooth adapter to a stable state.

If the device continues to fail to receive signal strength readings a Bluetooth beacon, the beacon might not be emitting signal due to a depleted battery, in which case the battery must be replaced.  It is also possible that a Bluetooth beacon has not been awakened properly, which can be resolved by tapping the beacon multiple times until an audio chime sounds.


##Over-the-air Updates

Your device has been added as a beta tester of the Minimap application.  The RIT North Star team will provide more detailed installation instructions should an over-the-air update be necessary.  Please note that it takes several hours for an update to become available in the Google Play Store after it has been added by the developer.

Except when instructed to by the team, do not attempt to remove or uninstall the Minimap application from the device.


#Control

This insatller package will install the Minimap Control Suite on your computer.  Minimap requires .NET 4.0 to run, which is likely already installed.  If not, the installer should ask you whether you'd like it to be installed automatically.
Once unpacked, it will place two icons on your desktop, one each for Bridge and Cartographer.  The Bridge shortcut will automatically request Administrator privileges (required for the server to run), so please use that.

The files you’ll need/use:

* An image with the layout of the venue in .PNG or .JPG form.  To work properly, the image must be cropped directly to the dimensions that you’re prompted to enter.  To do this, you can use pretty much any photo editing software (Photo Gallery, Lightroom) or even an online tool (e.g. lunapic.com/editor).
* A beacon specifications file (.BCN).  Each beacon has two types of identifiers, one that’s easily read by humans (a physical label that we’ve written on the beacons) and one that’s a somewhat messy hex code (like “E4:3E:A0:63:BC:C6”).  To save you the trouble, we’ve supplied a .BCN file with the IDs for the eight beacons we’ve sent.
* A Minimap map file.  This what you’ll be making with Cartographer, and will open in Bridge.  Instructions for creating it are below.

The process for creating a map using Cartographer:

1. Open the map image background, and specify some data (width and height in feet, name of the map)
2. Using the “Beacons” menu, add the beacon data (.BCN)
3. Construct the map.  There are four tools: pointer, barriers, tables, and beacons.
a. Pointer – same as you might expect in any painting application, use this to select, move, and resize a drawn object.
b. Barriers –Just click and drag to mark an area.
c. Tables – Rather than drawing each table individually, draw around each “block” of tables, and use the buttons at the bottom of the screen to indicate how they’re subdivided.
d. Beacons – Just place these where you want.  Once you’ve placed your beacons on the map, use the Pointer tool to select them, and assign their IDs using the selector in the bottom-right corner.

To use Bridge:

0. Run it as Administrator!
1. Open the map you made earlier in Cartographer.  Sometimes, it doesn’t draw right away.  If that happens, twitch something (a scrollbar, resize the window slightly, etc.) and it’ll trigger the redraw function.  We’re currently working on isolating this issue.
2. By default, it adds two “test” teams and fake judges, but you’ll want to add your own.  Go to Minimap -> Settings to configure them how you’d like.
3. Go to Server -> Start to fire up the server.  If you didn’t run Bridge as Administrator, it will not work.
4. Once you’ve done these three steps, users on the Android app can join a team, and they’ll show up in the Judges panel when you press refresh.
