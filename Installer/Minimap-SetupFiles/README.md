Minimap Information
============

This package will install the Minimap Control Suite on your computer.  Minimap requires .NET 4.0 to run, which is likely already installed.  If not, the installer should ask you whether you'd like it to be installed automatically.
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
