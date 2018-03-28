# MeeseeksBox

This project is meant to be a full transformation of the PirateBox project. It has been tested with a Raspberry Pi 3B and Zero W.

## Installation

1. Install PirateBox

2. Download the needed file
	1. For MacOS and Linux
    	- cd ~/Desktop/ && git clone https://github.com/digigon1/MeeseeksBox && zip -r MeeseeksBox.zip zip -r MeeseeksBox -x "*.DS_Store" && rm -fr MeeseeksBox && echo “script complete” && exit
	2. For Windows
		- Use of a bash port is recommended, follow the Linux instructions after it is installed
		
3. Connect to your PirateBox 
    1. Connect via SSH by following the instructions [here]( https://piratebox.cc/raspberry_pi:diy#installation)
    2. Connect using a keyboard
    
4. Copy MeeseeksBox.zip to the Pi 
	1. Through the Piratebox installation
    	- Connect to your Piratebox and upload MeeseeksBox.zip using the original piratebox browser 
    	- Drag and drop MeeseeksBox.zip to the NO NAME partition after imaging your card
    2. Using scp
    	- Send the file to the Piratebox by using the scp command (scp MeeseeksBox.zip alarm@piratebox.lan:~)

5. Find your file #If you uploaded using the browser your output should be similar
    - sudo find / -name MeeseeksBox.zip
        - Example output:
        -  [alarm@alarmpi ~]$ find -name MeeseeksBox.zip
        - /opt/piratebox/share/Shared/MeeseeksBox.zip 

6. Move MeeseeksBox.zip to the appropriate directory and unzip your file.
    - Example command:
    - sudo mv /opt/piratebox/share/Shared/MeeseeksBox.zip /home/alarm/ && cd /home/alarm && sudo unzip MeeseeksBox.zip

7. Run the install script. 
    - cd MeeseeksBox/files && sudo chmod +x install.sh && sudo ./install.sh

8. Reboot your Piratebox and connect to your MeeseeksBox!
