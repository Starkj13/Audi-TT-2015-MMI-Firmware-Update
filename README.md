# Audi-TT-2015-MMI-Firmware-Update

Hi, I just wanted to share my experience updating the MMI Firmware on my Audi TT MY2015.

## Requirements before starting:
- SD card 32 GB, Filesystem FAT32
- Firmware: [MIB Solution](https://mibsolution.one)
- MIB tool: [GitHub - Mr-MIBonk/M.I.B.](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki)
- Map file: [MIB Helper](https://mib-helper.com/)
- Hidden menus, REM, GEM menu: [GitHub - Mr-MIBonk/M.I.B.](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/%22hidden-menus%22---key-combinations)

## MMI Firmware update:

### Step 1: Check the current firmware version
- Open the Red Engineering Menu (REM), Open as the [key combination link](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/%22hidden-menus%22---key-combinations) shows or maybe Back button + the button on the left side of the Touchdail in the middle. My version was an old `MHI2_ER_AUG24_S0530 MU_0139` version.

### Step 2: Check the latest firmware version
- Enter the firmware version in [MIB Helper](https://mib-helper.com/) to check the latest version.
- If you have the same version that I started with `MHI2_ER_AUG24_S0530 MU_0139`, note that the website has the wrong firmware version suggested.
- You will get the error message "Train is blocked" if you try and install it. I found this Post from [Slons](https://www.digital-eliteboard.com/threads/audi-tt-mib2-mhi2-aug24-au43-firmware-update-und-ifs-root-el-patch.502191/post-3966881) that said you needed to update to `MHI2-ER-AU43x-P4204-MU1169` then go up to latest `MHI2-ER-AU43x-P5098-MU1339`. This worked for me. 

### Step 3: Download the latest supported firmware
- Download from [MIB Solution](https://mibsolution.one) (username: guest, password: guest).
- Transfer the content from the zip file to the root of the SD card formated FAT32.

### Step 4: Update the firmware
- Use the REM menu to update the firmware.
- Repeat steps 3 and 4 if needed to update from `MHI2_ER_AUG24_S0530 MU_0139` as shown in step 2.

### Step 5: Finish the firmware update
- You are done updating the MMI Firmware.

## Map License Update:

### Step 1: Patch the firmware with MIB tool
- Download the MIB tool from [GitHub - Mr-MIBonk/M.I.B.](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash).
- Download the Patched Firmware from [MIB Solution](https://mibsolution.one) (username: guest, password: guest).
- Extract the MIB tool and the Patch zip file.
- Place the MIB tool files on the root of the SD card.
- Place the Patch file in the Patch folder of MIB Tool.

### Step 2: Install MIB tool
- Use the REM menu to install the MIB tool. This process takes some time with reboots.

### Step 3: Access the Green Engineering Menu (GEM)
- This is a tricky bit. Get access to the Green Engineering Menu (GEM). People say to just press forward NAV/MAP and RADIO button in 5-10 seconds starting with NAV/MAP.
- But this didn't work for me, I needed to go to Setting --> System update and in there do the key compensation NAV/MAP and Radio. To get access to GEM.

### Step 4: Flash the patch image
- In GEM menu, go to `MIB.patch_ifs_root_aio` and select `Flash patch image`.
- Wait for the patch to finish (10-15 minutes).

### Step 5: Backup and update map files
- Backup the SD card files onto a computer.
- Download the latest Map file from [MIB Helper](https://mib-helper.com/). Enter your MMI version and find the Map files.
- Transfer the Map file to the SD card.
- Update the Map using the default system menu and system update. This takes about 20-30 minutes.

## Sources:
- Kip Hakes: [YouTube](https://www.youtube.com/watch?v=1nrXMcUg4cs)
- MIB Wiki: [GitHub - Mr-MIBonk/M.I.B.](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki)
- Firmware files: [MIB Solution](https://mibsolution.one) PS: Not the fastest servers, can take time.
- Slons: [Digital Eliteboard](https://www.digital-eliteboard.com/threads/audi-tt-mib2-mhi2-aug24-au43-firmware-update-und-ifs-root-el-patch.502191/post-3966881)
- TTForum.cu.uk Firmware Discussion: [TTForum](https://www.ttforum.co.uk/threads/firmware-updates.1970533/?post_id=9355899&nested_view=1&sortby=oldest#post-9355899)
- Hidden menus: [GitHub - Mr-MIBonk/M.I.B.](https://github.com/Mr-MIBonk/M.I.B._More-Incredible-Bash/wiki/%22hidden-menus%22---key-combinations)
