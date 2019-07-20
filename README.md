# TeslaCam

## TL;DR
Use one USB stick for both dashcam and media in your Tesla.

![][grandpa]
**HERE BE DRAGONS! THIS PROCESS WILL DELETE ALL CONTENTS ON THAT USB STICK WHEN WE GO THROUGH THIS. HAVE A BACKUP OR COPY THE CONTENTS OF IT, BEFORE WE START, IF YOU NEED TO. I WILL NOT TOLERATE TEARS OF SADNESS FOR YOU DELETING [insert important stuff here] FROM THE USB DISK.**

## The longer what
The point of this guide is to show how you can use 1 usb stick for both TeslaCam and Media. Saving one precious port is great!

The solution is to partition the USB disk into two partitions, one for TeslaCam and one for Media.

I have found that a USB stick with both a TeslaCam folder and Media on the same disk, is not recognized as other than a dashcam recorder.

This is for Mac OS. Windows will follow later. It is far easier on Windows.

## The How-to
There a a few steps to make this work, especially on Mac OS. Windows is much simpler. Use the disk Management tool to partition the disks. I'll make a guide later for that, but on a Mac it is a bit more cumbersome.

### Steps
1. Set up Disk Utility for this
1. Format the drive to Mac format
1. Add partitions
1. Format those partitions to MS DOS
1. Add content and folders
1. Drive

## 1. Set up Disk Utility
Insert your USB stick.

Remember the old man yelling up top. Backup. OK? Can we go on now? Thank you.

Start Disk Utility on your Mac. It is located in /Applications/Utilities. The fastest way is just to do a Spotlight search for `Disk Utility` and start it.

![][spotlight]

By default Disk Utility will not show all devices, only defined partitions on those devices. We need to change that.

Either go to `View > Show All Devices` or tap the View button in the top left corner ad set it to `Show all devices`. Keyboard shortcut is `cmd + 2`.

Your window should look a bit like the one below now. Your disk names will differ.
![][default-disk]


## 1. Format the drive
Now we need to split the USB Drive into two parts. There is an icon in the toolbar called partition, but it will be greyed out, if this is a Windows formatted USB disk.

In your sidebar there will be a grouping of `Internal` and `External` disks. Your USB disk is in the `External` group.

**DO. NOT! PICK! OR! TOUCH! THE! INTERNAL! GROUP!** That is your main harddrive.

Pick the top most device for your USB drive. Most likely it is the only one there, but if you have external harddrives connected, they may show up there as well. Yank those out for now if you are unsure. Better safe than stupid I always say.

After selecting your top most device in the `External` group, click the Erase icon in the toolbar

![][erase-disk]

Change the settings to the following.
- Name: Untitled
- Format: Mac OS Extended (Journaled)
- Scheme: GUID Partition Map

Ok. This is it. Once you press that Erase button, all files on this usb drive is deleted. Go on. Push it. You know you want to.

![][push]

## Add partitions
Now we will do the actual partitioning.
Pick the Untitled disk, and now select the Partition icon in the toolbar. It will bring up a new dialog inside Disk Utility, which lets you decide stuff!

![][partition]

Press '+' sign to add a new partition.

TeslaCam part should be the first. I have set the TeslaCam part (tesla) to be 48 GB, and the media to be the rest. You can drag the small circles on the outer edge to resize the partitions.

The right hand side part of this circle needs to be the TeslaCam partition.

Set both partitions to Mac OS Extended. And press apply. The computer will do it's thing and puny humans are instructed to wait. So we wait.

## Format as MS-DOS (FAT)
After the partition is done, the partitions need to be formatted to MS-DOS (FAT). Disk Utility on Mac can't do this while partitioning for some reason.

To do this correctly, eject the two partitions, you just created, by clicking on ⏏️ symbol beside both names. After a while they will both be greyed out.

If you don't unmount the disks, the formatting will fail.

![][format error mounted]

Now it is straight forward to format the disks one by one.

![][format]

You are now done, and you can copy the content you want to the media part.

![][copy]

Remember to make a folder in the Tesla part called 'TeslaCam'.
![][folder]

Now, plug in and drive your Tesla!

[erase-disk]: erase-disk.png "Formatting works"
[format error mounted]: format-error-unmounted.png  "remember to unmount the volumes"
[copy]: copy.png "Copying 23 items"
[folder]: teslacam.png
[default-disk]: default-disk-utility.png
[grandpa]: grandpa.gif
[format]: format.png
[push]: pushbutton.gif
[partition]: partition.png
[spotlight]: spotlight.png