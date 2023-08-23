---
layout: single
tags:
  - table of contents
toc: true
toc_sticky: true
title: ""
author_profile: false
sidebar:
- title: "Download GRASS Binary Apps for the Macintosh"
  image: assets/images/grasslogo.svg
  image_alt: "image"
  text: "Current stable, development, and legacy binary apps"
---
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-9NBX5KDKM0"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-9NBX5KDKM0');
</script>

## GRASS Software: Stable Releases

| Version | Date | Download Link | Configuration Info|
| :--- | ---: | :---: | :---: |
| GRASS 8.3.0 Apple ARM | 24 Jun 2023 | [download](http://download.osgeo.org/grass/mac/grass-8.3.0-arm64.dmg) | [download](http://download.osgeo.org/grass/mac/grass-8.3.0_configure_info.txt){:target="_blank"} |
| GRASS 8.3.0 Intel | 24 Jun 2023 | [download](http://download.osgeo.org/grass/mac/grass-8.3.0-x86_64.dmg) | [download](http://download.osgeo.org/grass/mac/grass-8.3.0_configure_info.txt){:target="_blank"} |
| GRASS 8.2.1 Apple ARM | 3 Apr 2023 | [download](http://download.osgeo.org/grass/mac/grass-8.2.1-arm64.dmg) | [download](http://download.osgeo.org/grass/mac/grass-8.2.1-arm64_configure_info.txt){:target="_blank"} |
| GRASS 8.2.1 Intel | 23 Jan 2023 | [download](http://download.osgeo.org/grass/mac/grass-8.2.1-x86_64.dmg) | [download](http://download.osgeo.org/grass/mac/grass-8.2.1_configure_info.txt){:target="_blank"} |
| GRASS 7.8.8 Apple ARM | 14 Aug 2023 | [download](http://download.osgeo.org/grass/mac/grass-7.8.8-arm64.dmg) | [download](http://download.osgeo.org/grass/mac/grass-7.8.8_configure_info.txt){:target="_blank"}  |
| GRASS 7.8.6 Intel | 14 Aug 2023 | [download](http://download.osgeo.org/grass/mac/grass-7.8.8-x86_64.dmg) | [download](http://download.osgeo.org/grass/mac/grass-7.8.8_configure_info.txt){:target="_blank"}  |

## GRASS Software: Development Releases

| Version | Date | Download Link | Configuration Info|
| :--- | ---: | :---: | :---: |
| GRASS 8.4dev Apple ARM | 14 Aug 2023 | [download](http://download.osgeo.org/grass/mac/grass-8.4.0dev-arm64.dmg) | [download](http://download.osgeo.org/grass/mac/grass-8.4dev_configure_info.txt){:target="_blank"} |
| GRASS 8.4dev Intel | 14 Aug 2023 | [download](http://download.osgeo.org/grass/mac/grass-8.4.0dev-x86_64.dmg) | [download](http://download.osgeo.org/grass/mac/grass-8.4dev_configure_info.txt){:target="_blank"} |

### Features of Note
***New Native Support for Apple ARM Processors***
Thanks again to Nicklas Larsson for updating his build scripts to support the new, fast Apple ARM processors. Current versions to support prior Intel processors are also available.

***All Dependencies Included***  
These GRASS apps are packaged with all needed dependencies, which are detailed in an accompanying *configuration info* file. They include correct versions of Python and wxPython to run: Python 3 and wxPython 4 for GRASS versions 7.8 and higher, and Python 2.7 and wxPython v3 or 4 for earlier versions. Hopefully this will avoid any conflicts with other versions of GRASS dependencies you may have intentionally or inadvertently installed with other apps, and will run without needing to disable OS X System Integrity Protection.

***Mac OS X support***  
These newest apps were built under macOS 12 (AKA Monterey). I don't know which older Mac OS versions will run this app--probably OS X 10.13 and above, possibly older OS X versions.

***International Language Support***  
These versions of GRASS are compiled with international support for multiple languages (gettext).

***LiDAR Processing Support***  
Versions 7.8.6dev and higher are now compiled with **libLAS** so that all GRASS LiDAR processing tools work within the GRASS environment. PDAL support is catching up in GRASS 8.

GRASS versions 7.8.3 and above are compiled with **PDAL** library support for reading and manipulating LAS LiDAR files within GRASS. For some reason, the input module (v.in.pdal) does not show up in the menus in GRASS 7 (it does in GRASS 8). You'll have to run it from the terminal or console (v.in.pdal&). Command line PDAL tools can also be run from the GRASS terminal. I also have bundled the **LAStools** command line utilities which you can run from the command line. These utility programs allow you to read/write LAS (lasinfo, las2las, las2txt, txt2las) and LAZip files (laszip), do filtering and processing (lasdiff, lasindex, lasmerge, lasprecision), and translate them into csv formats that GRASS can read (las2txt).

***Advanced Features in GRASS 8***  
GRASS 8 now includes a new **data catalog** window that provides a much easier way to manage and access GRASS data directories, locations, and maps. This is a major enhancement in usability. Note that it will not recognize your GRASS 7 configuration files and you'll have to respecify your database and any other preferences.  
(**Alert** If you happen to have a filename of a 2D or 3D map with the "@" symbol, the data catalog will fail and only partly open at start up, but there is no error message).

GRASS 8.3 has a new **single window GUI interface**. This is the most significant change in the GUI since GRASS 6. It is nicely organized, with all GRASS features as panes within a single window that you can place and resize on the desktop. If you like the look of QGIS or ArcGIS, or regularly use Linux or Windows, this may be just the thing for you. If you prefer the older, more Mac-like multi-window interface, you return to that by hecking the box for it in preferences/general and closing/restarting the GUI (type g.gui from the terminal after closing the GUI).

### Installing GRASS for Mac  
1. Download and unzip the *.dmg installation package  
2. Drag the GRASS app to your /Applications folder (it will not work properly in any other folder)

#### Installation tips
***Installation location***  
These new fully bundled binaries **MUST** be installed and run from the /Applications folder. They will not run from another folder or even a subfolder of /Applications. This has to do with the build environment. If this changes, I'll note it here.

***First time launch of a GRASS app***  
Current stable and preview versions of GRASS should launch without any special permissions issues (see below). Sometimes it seems to take a long time to open the app the first time (this seems kind of random). So be patient and look for the little dialog box that asks you if GRASS can control your terminal--answer yes. After the first time, each app should open quickly and without issue.

Because I do not have permission to authenticate ("sign") Mac apps, older version of these binaries may fail Apple's verification test. To run them, you ***may*** need to control-click the app and select "**open**" the first time you run an app you have downloaded. After verification fails, you will be given the option to "open" the app anyway. You only have to do this once for each app or version you download. I and others have noticed that after doing this, the app may close and you will have to double click it again, and it may take some time to launch initially. After the first time, each app should open quickly and without issue.

***Installing GRASS extension***  
Extensions written in pure Python will install without any problems. If an extension is in a language that needs to be compiled (e.g., C or C++), you must have Apple's Command Line Tools installed. You can do this in a couple of ways.

1. You can install the full Xcode package (quite large). Once it opens, install the Developer Command Line tools from the Xcode menu.  
2. You can just install the Command Line Tools from the terminal, without installing the full Xcode package. Launch a terminal window (The terminal app is found in the /Applications/Utilities folder). Type the following, followed by a return.

```
xcode-select —install
```

The next time you launch GRASS, you should be able to install and compile any extension.

Please report any bugs in the [GRASS issue tracker](https://github.com/OSGeo/grass/issues){:target="_blank"}.  

## Legacy GRASS apps (will not be further updated)
These releases require you to have installed needed ***[frameworks](download-frameworks.md)***  (AKA dependencies or helper programs) before installing GRASS for the first time. Check the frameworks page to make sure you have the appropriate framework versions.

Legacy GRASS binaries from this site may not work with OS X 10.11 (*El Capitan*) and above unless you disable "System Integrity Protection". A workaround to allow GRASS to run is provided below.

### Selected legacy binaries for OSX 10.8+  
These versions of GRASS are compiled with international support (gettext) and LiDAR (LASlib and tools) support. As far as I can tell, they work with Mac OS X version 10.8 (AKA "Lion") and above if System Integrity Protection is disabled.

| Version | Date | Download Link |
| :--- | ---: | :---: |
| GRASS 7.6.2 64bit wxPython 3 | 8 Aug 2018 |[download](http://download.osgeo.org/grass/mac/grass-7.6.2.dmg.zip) |
| GRASS 7.3 64bit wxPython 3  | 13 June 2016 | [download](http://download.osgeo.org/grass/mac/GRASS-7.3_64bit_wxp3.pkg.zip) |
| GRASS 7.3 development  | 14 Sept 2016 | [download](http://download.osgeo.org/grass/mac/GRASS-7.3_2016-09.pkg.zip) |
| GRASS 7.2 development  | 14 Sept 2016 | [download](http://download.osgeo.org/grass/mac/GRASS-7.2svn.pkg.zip) |
| GRASS 7.0.5 stable  |  3 Oct 2016 | [download](http://download.osgeo.org/grass/mac/GRASS-7.0.5.pkg.zip) |
| GRASS 6.4.6 svn  | 28 Apr 2016 | [download](http://download.osgeo.org/grass/mac/GRASS-6.4svn.pkg.zip) |

### Selected legacy binaries for OSX 10.6+  
These even older binaries for 10.6 seem to also run well with 10.8 and maybe above. However, they are based on system Python 2.5 and 2.6.

| Version | Date | Download Link |
| :--- | ---: | :---: |
| GRASS 7.0 dev | 1 November 2013  | [download](http://download.osgeo.org/grass/mac/GRASS-7.0svn.pkg.zip) |
| GRASS 6.5 dev | 31 October 2013 | [download](http://download.osgeo.org/grass/mac/GRASS-6.5.pkg.zip) |
| GRASS 6.4.3 stable | 30 July 2013 | [download](http://download.osgeo.org/grass/mac/GRASS-6.4.3.pkg.zip) |

**An archive of all GRASS binaries I've compiled for the Mac can be found on the [OSGEO server for GRASS for Mac binaries](http://download.osgeo.org/grass/mac/)**

### Known bugs in legacy versions  
There are several known bugs to watch out for that affect the GUI:  
1. The Wizard to create a custom location (projection/CRC) was broken in version 7.8.5. It is fixed in 7.8.6 and above. Other methods of creating a location work.  
2. The digitizer module and the interactive supervised classification module (for satellite imagery) were unstable and crashed the GUI in older versions. You would need to restart the GUI by typing 'g.gui' into the terminal and hitting return. The raster digitizer was now working well in GRASS 7.5 but the vector digitizer was still broken. All is now fixed in GRASS 7.8 and above.  
3. In GRASS 7.2.2, a few drop down controls (entry widgets) did not recognize mouse clicks. You need to use your arrow keys or type the entry for them to work. This is fixed in the later versions of GRASS.  
4. In GRASS 7.2.2, when switching back from the 3D interface to the 2D interface, one of the 3D window control buttons (for fly through) will overwrite one of the 2D menu buttons (zoom to max). If you click this overwritten button, the GUI will crash and you will have to restart it (see #1). This is fixed in the later versions of GRASS.

### Installing and running legacy binaries
**2-step installation of legacy GRASS binaries for the Mac**
1. You need to download and install some helper programs, called *frameworks* (the same as "dependencies" on Linux systems). I've provided these as compiled packages on the **[frameworks page](https://cmbarton.github.io/grass-mac/_pages/download-frameworks.md)**. William Kyngesburye compiled these frameworks and also has a [page with legacy frameworks](https://www.kyngchaos.com/software/){:target="_blank"}. You can find the latest versions there. Be advised that the newest versions of these frameworks may not work with older legacy GRASS binaries. This is one of the reasons I switched to fully packaged apps with all such dependencies included.
2. Then you just need to download one of the GRASS binaries above. Each downloaded app comes as a compressed disk image (**.zip* expanded to **.pkg*). You just double click and follow the instructions. Although these binaries automatically install directly into the Mac Applications folder, you can move them to another folder of your choice.

**How to alter system settings in OS X 10.11 (El Capitan) and newer so that older GRASS binaries will run**  
This is a work around that seems to allow you to run GRASS on a Mac after upgrading to the new Apple OS. It involves disabling a new *System Integrity Protection* feature. This reduces security of your system to the level it was before the El Capitan OS X release.

1. Restart your Mac in *Recovery Mode*. To do this, choose **Restart** from the Apple menu, and as soon as the screen turns black hold down **Command + R** on the keyboard until the Apple logo appears on your screen.  
2. Select **Terminal** from the Utilities menu.  
3. In the Terminal Window that opens type: **csrutil disable**  
4. Press the **Return** key.  
5. Choose **Restart** from the Apple menu.

To reenable System Integrity Protection, follow the above steps but in the terminal, type: **csrutil enable**

Some people may need to reinstall frameworks for GRASS to run. For others, this is not necessary
