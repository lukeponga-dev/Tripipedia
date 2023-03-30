
[b] Encrypted Ubuntu Linux Host[/b]

[i]We have chosen Ubuntu 21.10 as our host operating system for all of our Tutorials - the reason being is that its the most widely supported Linux OS that has drivers and firmware support for most devices. Other Linux Flavors are available but for the normal new Linux user who wishes to not use Windows - This is by far the best way to go. There is nothing worse than installing a new Operating System only to find some of your devices do not work.


For this Tutorial and for best NETSEC and OPSEC Practice. We are going to run the Host install from an External Encrypted Drive (SD / NvMe) are preferred as at any stage we can rip out the SD / NvMe and snap it in half or hit it with a hammer.[/i]

[b]What we will need for this tutorial is a Computer and 2 External Drives as noted above.[/b]

[b]Download The latest version of Ubuntu:[/b] 
[i]At the time of writing The latest version is 21.10[/i]

1: Open your web browser preferably using a Proxy and navigate to: *** CLEARNET https://ubuntu-mate.org/download/amd64/impish/ CLEARNET ***
2: Choose the method youd like to use (Direct Download or Torrent) - The preferred method of download is using the torrent option as it has a hash check which verifies the integrity of the .iso
3: Once the file is downloaded verify using the instructions listed here: *** CLEARNET https://ubuntu-mate.org/faq/verify-download-quick/ CLEARNET ***
4: Save the Image to your machine and write it to your first External Drive. 
5: If using Windows youll need (Etcher) 
6: If using Linux (usb-creator-gtk) which can be installed with 
[code]sudo apt install usb-creator-gtk[/code]

[i][b]Now that you have your installation media created its time to boot from the drive:[/b][/i]

[b]INSTALL UBUNTU:[/b]

[b]1:[/b] Reboot your machine and boot into the bios and turn off secure boot. We want to do this so that the install does not enroll a key into your bios.
[b]2:[/b] Usually the bios can be accessed by pressing the DEL / ESC / F2 Key
[b]3:[/b] Once that is done save and exit the Bios by pressing the F10 key and save the changes.
[b]4:[/b] As soon your machine reboots press the boot menu key so we can boot from the SD card we created. On most machines its F12 / F11 / F8 - Consult your computer brand for how to do this if none of them work.
[b]5:[/b] The Ubuntu boot menu will appear and you can select the first option and you should boot into live mode of the OS
[b]6:[/b] Once booted you will have a the option to Try Ubuntu Mate / Install and the Select your preferred language menu
[b]7:[/b] Next you will be prompted to select your keyboard Layout - Choose the layout that you use and click next
[b]8:[/b] Next on the Updates and Software Screen you will have the option for Normal or Minimal Installation. Select Minimal
[b]9:[/b] Put a checkbox in both download updates and Install Third Party Software
[b]10:[/b] If you have a Configure secure boot checkbox then you know you have not disabled secure boot in the bios (quit the installation and reboot back into your bios in step 1)
[b]11:[/b] Next the installation type window will appear
[b]12:[/b] Select Erase Disk and Install Ubuntu Mate and click the advanced Features Button
[b]13:[/b] A little window will pop up / Select the Encryption type you'd like to use - The preferred method is ZFS
[b]14:[/b] Put a tick in the Encrypt the new Ubuntu Mate Installation and click OK and then Continue
[b]15:[/b] You will now need to choose a password for your encryption to unlock your drive at boot. Enter a nice long passphrase that you will remember and click Install Now
[b]16:[/b] Now you will have the option to select the disk you'd like to install onto. Select the second external drive that you had inserted at boot - MAKE SURE YOU SELECT THE CORRECT DRIVE..
[b]16:[/b] MAKE SURE YOU SELECT THE CORRECT DRIVE.. (yes!! check twice)
[b]17:[/b] Click the install now - A window will pop up detailing the changes that will be made to your disk.. Click Continue. 
[b]18:[/b] The next window will ask for your location and then click continue
[b]19:[/b] On the Who are you Screen input your details. Obviously don't use your real name here. and ensure you select Require Password to Login.
[b]20:[/b] Press Continue and then sit back and relax while the installation finishes. 
[b]21:[/b] Once the installation has completed you will need to reboot your machine. Press the restart button and remove your installation media.

[b]BOOTING FOR THE FIRST TIME:[/b]

[b]1:[/b] Once the machine reboots press the F12 / F11 / F8 boot menu key and select your second external USB card.
[b]2:[/b] You will be prompted with a Decrypt Disk Passphrase prompt. Input the password you used in step 15 above and press enter.
[b]3:[/b] Your machine will boot and you will be presented with the login Screen.
[b]4:[/b] Login and you will then be presented with the desktop which will be your base for the remaining Linux tutorials.

Familiarize yourself with the layout etc. 
You can navigate to the top left menu and go down to the Control Center where you can make changes to your settings and install additional drivers.

For the most part of using Linux we are going to be using the command line a lot so a good idea is to add the Terminal Launcher to your top bar. 
[b]
To do this:[/b]
[b]1:[/b] Click on the Menu and select System Tools. You will see MATE terminal listed. 
[b]2:[/b] Select it and drag it to your top bar.
Once on the top bar. Click it and type:

[code]sudo apt update 
sudo apt-dist upgrade -y
sudo reboot -n[/code]

Your machine will reboot and you will have a fresh clean O/S updated and ready to use.
