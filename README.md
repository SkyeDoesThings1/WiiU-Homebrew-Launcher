# I have no idea what I'm doing this is a learning project for me cause I thought it would be easy I'd be surprised if this went ANYWHERE lmao

# WiiU Homebrew Launcher RPX

The Homebrew Launcher is a WiiU homebrew that lists homebrew applications located on a SD card and permits launching them (similar to the Homebrew Channel of the Wii).

#### Usage

To use the Homebrew Launcher (or HBL, for short) you must copy homebrew_launcher.rpx into SD:/wiiu/apps/homebrew_launcher/homebrew_launcher.rpx.

To start the Homebrew Launcher you need to run [MochaLite](https://github.com/wiiu-env/MochaLite) and open the "Health and Safety"-app.

The apps that will be listed are should be in the following path /wiiu/apps/homebrew_name/some_elf_name.rpx on the root of the SD card. A meta.xml and an icon.png (256x96) are optional. Here is an example:

- sd:/
  - wiiu/
    - apps/
     - homebrew_launcher/
        - homebrew_launcher.rpx
        - meta.xml
        - icon.png
     - loadiine_gx2/
       - loadiine_gx2.rpx
       - meta.xml
       - icon.png
     - ddd/
       - ddd.rpx
       - meta.xml
       - icon.png
     - ftpiiu/
       - ftpiiu.rpx
       - meta.xml
       - icon.png

#### Building the Homebrew Launcher
To build the main application devkitPPC is required as well as some additionally libraries. If not yet done export the path of devkitPPC and devkitPro to the evironment variables DEVKITPRO and DEVKITPPC. 

Make sure you have [wut](https://github.com/devkitPro/wut/) installed.

In addition you need: 
- [libgui](https://github.com/wiiu-env/libgui) for the gui elements.
- The ppc-portlibs `pacman -Syu ppc-portlibs`

All remaining is to enter the main application path and enter "make". You should get a homebrew_launcher.rpx in the main path.

#### Building an applicationfor the Homebrew Launcher 
For an example on how to build an application for the HBL check out the [wut samples](https://github.com/devkitPro/wut/tree/master/samples).

#### Meta XML

The meta.xml is optional and can be put in the same path as the homebrew ELF file to display additional information about the homebrew.

Here is a XML example:

    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <app version="1">
    <name>name</name>
    <coder>coder<coder>
    <version>app version</version>
    <release_date>app release date</release_date>
    <short_description>short description</short_description> 
    <long_description>long description</long_description> 
    </app>

#### Icon PNG
The icon.png has to be of the resolution 256 x 96 and can be placed in the same path as the homebrew ELF file. This file is optional and shows an icon for the homebrew inside the homebrew launcher.

### Credits
* Dimok
* orboditilt
* many contributors with their pull requests

##### WUT RPX toolchain which is used to build RPX version of HBL
* exjam
* shinyquagsire23
* several more contributors

##### HBL channel artwork / boot sound and video
* cathor
* Maschell
