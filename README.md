# Audi-TT-2015-MMI-Firmware-Update


Hi, I just wanted to share my experience updating the MMI Firmware on my Audi TT MY2015.

Requirements before starting:

SD card 32 GB, Filesystem FAT32

Firmware: https://mibsolution.one

MIB tool: https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki

Map file: https://mib-helper.com/

Hidden menus, REM, GEM menu: https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/%22hidden-menus%22---key-combinations

MMI Firmware update:

First step was to check the firmware version that is installed. To check this, you open the Red Engineering Menu (REM), Open as the key combination link shows or maybe Back button + the button on the left side of the Touchdail in the middle. My version was an old MHI2_ER_AUG24_S0530 MU_0139 version.

Check the latest version by entering the firmware version in https://mib-helper.com/. IF you have the same version that I started with MHI2_ER_AUG24_S0530 MU_0139. The website has the wrong firmware suggested, you will get the error message "Train is blocked". I found this Post from Slons said you needed to update to MHI2-ER-AU43x-P4204-MU1169 then go up to latest MHI2-ER-AU43x-P5098-MU1339. This worked for me

Download the latest supported firmware from https://mibsolution.one, guest guest. Then transfer the content from the zip file to the Root of the SD card.

Update the firmware by the REM menu.

Do 3 and 4 again if needed to update from MHI2_ER_AUG24_S0530 MU_0139 as shown in step 2.

You are done updating MMI Firmware.


Map License Update:

If you want lifetime map license, you need to Patch the firmware with MIB tool: https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash

Download MIB tool from GitHub. Download the Patched Firmware from https://mibsolution.one, guest guest.

Extract the MIB tool and the Patch zip file and place the MIB tool files on the Root of the SD card. Place the Patch file in the Patch folder of MIB Tool.

Install MIB tool by REM menu, takes some time with reboots.

his is a tricky bit. Get access to the Green Engineering Menu (GEM). People say to just press forward NAV/MAP and RADIO button in 5-10 seconds starting with NAV/MAP. But this didn't work for me, I needed to go to Setting --> System update and in there do the key compensation NAV/MAP and Radio.

When in GEM menu go in too MIB. patch_ifs_root_aio --> Flash patch image.

Wait for the Patch to finish, 10-15 min.

Now you have a patch firmware.

Backup the SD card files on to a computer.

Download the latest Map filet from https://mib-helper.com/, Enter your MMI version and further down you have the Map files.

Transfer the Map file to the SD card. Update the Map by the default system menu and system update.

What 20-30 min to the map to update.

Sources:

Kip Hakes: https://www.youtube.com/watch?v=1nrXMcUg4cs

MIB Wiki: https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki

Firmware files: https://mibsolution.one

Slons: https://www.digital-eliteboard.com/threads/audi-tt-mib2-mhi2-aug24-au43-firmware-update-und-ifs-root-el-patch.502191/post-3966881

TTForum.cu.uk Firmware Discussion: https://www.ttforum.co.uk/threads/firmware-updates.1970533/?post_id=9355899&nested_view=1&sortby=oldest#post-9355899

Hidden menus: https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/%22hidden-menus%22---key-combinations
