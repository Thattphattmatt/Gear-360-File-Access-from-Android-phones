# Gear 360 File Access from Android phones
Samsung Gear 360 (2017 version) File Access from Android phones - works on even Android 11

**This project consists of 2 parts:**
1. Software mod on Samsung Gear 360 (installing provided files on SD card)
2. Android application from Google Play

## Aim of this project

Samsung stopped supporting their great 360 degree camera Gear 360. And the official Samsung Android app for accessing files on the camwera from the phone is not working on Android 11 or later because of the storage permission requirements on Android 11.
The official application still works for remote controlling the Gear 3460 camera, but as soon as we try to access the images or videos on camera the app crashes.

With this mod, I provide a solution to access camera images and videos. The http server on camera (**part 1**) will serve the files on OSC (Streetview mode)
And the android application will access the files, copy them to the phone. (**part 2**)

Application also stitches the images and videos to photosphere (360 panorama) format on user request (STITCH function)
After the stitch operation, metadata for identification of the files as 360 degree panorama is also injected to the jpg and mp4 files.

All images & videos copied from the camera are copied and saved on the phone's external storage Gear360 folder.
If stitching function is used, the stitched files are also saved on the same folder.

Video stitching takes a long time. I will work on making it faster if I can find a better method.

### Important !

This application is tested on Gear 360 2017 version. It may also work on the previous Gear 360 but not tested.

## Installation

### Part 1

Please clone this repository or download the .zip file of it. (If you're on GitHub, click the green "Clone or download" button on the right, and then "Download ZIP".)
Copy the contents of the SD-card-root folder to the root of the SD card you're using with your Gear 360 camera (2017).

Your SD card should now look like this:

    SD card root
    |-- DCIM
    |-- SYSTEM
    |-- info.tg
    |-- nx_cs.adj
    |-- mod.sh
    `-- mods
        |-- www
        |   |-- cgi-bin
        |   |    |-- files
        |   |    `-- gallery
        |   |-- index.html
        |   `-- top.html
        |-- jhead
        `-- httpd
            
    
    
DCIM and SYSTEM were put there by the camera. Everything else is the contents of the SD-card-root folder from this repository.
Put your SD card back in your Gear 360 camera (2017). And power it on.
After a few seconds you should see the front led of the camera blink (green-orange) for 2 seconds.
This confirms that the http server is running on camera.

### Part 2

Please install the Android application from Google Play. Name of the app is "Gear 360 File Access"
Dİrect URL to Google Play will be provided later here:
//TODO

