#### Hc32f460kct6 Marlin
HDSC package here:
https://github.com/ANYCUBIC-3D/HDSC_SupportPackage

## [Tutorial] How to build Anycubic Marlin source code into a firmware.bin

My previous poll got many yes so here is the tutorial.

### Requirements

A Windows computer
45 minutes of your time

### Tutorial

First of all, download and install Keil v5.36, do not install v5.37 as it doesn't ship with ARM Compiler v5.36 -> https://armkeil.blob.core.windows.net/eval/MDK536.EXE

Install the software as you would install any software and open it

The Pack Installer will open and start installing default packages (the progress bar is at the bottom right) . In the future if you want to open the Pack Installer it is located under Project -> Manage -> Pack Installer...

Once the default packages are installed, in the Pack tab on the right, find and install ARM::CMSIS 5.7.0 (2020-04-09) and uninstall the 5.8.0 version

https://preview.redd.it/ho2qky648kt91.png?width=328&format=png&auto=webp&s=37966a0a67e8c0ef7a0e40f1486322ad186620ed

Now, download and install HDSC.HC32F460 v1.0.7 -> https://1drv.ms/u/s!Ak69-GxOpF6Pg9gV3zWT5AIJPEan9g?e=ipQaD7

Once the installation is done, you can close the Pack Installer and open Keil µVision 5

Go to File -> License Management...

Click on Get LIC via Internet... and click OK

On the next page, enter this code in Product Serial # (PSN) -> 42B2L-JM9GY-LHN8C

Enter a PC Description, a First Name, a Last Name, an E-mail, your country and your phone (everything else should be optionnal). The E-mail will be used to send you your activation code so make sure to input a real E-mail!

Press Submit on the bottom and wait to receive the E-mail

In the E-mail you will get a License ID Code (LIC), copy that code and go back to Licence Management in µVision

Paste the LIC in the New License ID Code (LIC) input and press Add LIC

https://preview.redd.it/gszdo2ae8kt91.png?width=636&format=png&auto=webp&s=3585c6751889081a76616f337b56191703587315

Close the License Management tab and go to Project -> Open Project...

Open the anycubic.uvprojx file located in the workspace folder of the Anycubic source code (download it from Github)

You shouldn't have any error / message in the Build Output tab on the bottom, if it stays empty then it's good

To build, go to Project -> Build target

The output file will be located under workspace/firmware.bin

Enjoy
