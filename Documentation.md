# Introduction #

This patch removes certain software limits from video card drivers in Mac OS X.


# Who is this for? #

1) You want to connect a 4K monitor to HDMI on your Mac

2) You want to overclock your monitor

If you have a MacBook Pro with Retina Display, you will be able to drive a 4K monitor from its HDMI port.


# Supported OS X versions #
  * 10.7.4
  * 10.7.5
  * 10.8.3
  * 10.8.4
  * 10.8.5


# Supported video cards #
  * Many Intel video cards
  * Newer NVIDIA video cards

I tested this patch on 13" MacBook Pro with Retina Display and 15" MacBook Pro with Retina Display, but other systems should be supported as well.


# If something goes wrong #

Before you get started, make sure you have a Recovery partition on your Mac, just in case something goes wrong. When you boot your Mac, hold the option key and you should see an option to boot from a Recovery partition.

My patch creates a backup file in the same folder as the patched file; if you need to roll back, copy the backed up file (with .bak extension) over the patched file.

This patch changes the following files:

  * /System/Library/Frameworks/IOKit.framework/Versions/A/IOKit/IOKit
  * /System/Library/Extensions/NVDAGK100Hal.kext/Contents/MacOS/NVDAGK100Hal


# If your OS X version or video card is not supported #

Get in touch with me and I will see what I can do.


# How to install this patch #

Download it here: [mac-pixel-clock-patcher download link](http://mac-pixel-clock-patch.googlecode.com/git/macPixelClockPatcher.command)

Download it into your Downloads folder. Open Terminal and run:

**cd ~/Downloads**

**chmod +x macPixelClockPatcher.command**

**./macPixelClockPatcher.command**


You will be asked to enter your password to approve changes in your system.

Pay attention to the output - it should say it detected unpatched IOKit and NVIDIA driver on (your OS X version) and patch it.

Reboot your system.

After reboot, you should be able to get custom resolutions with over 165 MHz pixel clock to work using SwitchResX.


# After you install this patch #

Use SwitchResX to create a custom resolution to drive your screen at the resolution and refresh rate that you need: [SwitchResX download link](http://www.madrau.com/download/latest/latest.html)

Slowly increase the refresh rate to see how far your system can go.

For example, use the following settings when creating a custom resolution:

  * Use simplified settings - CVT-RB, 1920, 1080, 75 Hz. Test it.
  * Use simplified settings - CVT-RB, 1920, 1080, 85 Hz. Test it.
  * Use simplified settings - CVT-RB, 1920, 1080, 90 Hz. Test it.
  * Use simplified settings - CVT-RB, 1920, 1080, 95 Hz. Test it.
  * Use simplified settings - CVT-RB, 1920, 1080, 100 Hz. Test it.
  * Use simplified settings - CVT-RB, 1920, 1080, 105 Hz. Test it.
  * Use simplified settings - CVT-RB, 1920, 1080, 110 Hz. Test it.

Same for 4K:

  * Use simplified settings - CVT-RB, 3840, 2160, 16 Hz. Test it.
  * Use simplified settings - CVT-RB, 3840, 2160, 20 Hz. Test it.
  * Use simplified settings - CVT-RB, 3840, 2160, 22 Hz. Test it.
  * Use simplified settings - CVT-RB, 3840, 2160, 24 Hz. Test it.
  * Use simplified settings - CVT-RB, 3840, 2160, 26 Hz. Test it.
  * Use simplified settings - CVT-RB, 3840, 2160, 28 Hz. Test it.
  * Use simplified settings - CVT-RB, 3840, 2160, 30 Hz. Test it.
  * Use simplified settings - CVT-RB, 3840, 2160, 31 Hz. Test it.