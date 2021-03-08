# Java-gui-through-ssh
How to run Java Gui using xming on windows for mc to install clients. 

1. First you need to install xming from this website http://www.straightrunning.com/XmingNotes/
2. Once xming has installed onto your pc. Go to search bar and search for xming to open the server.
3. The server icon should appear on the right of the windows task bar where the date and time is. 
4. Next go to [Drive letter]\Program Files (x86)\Xming on your windows install and look for X0.hosts
5. Copy X0.hosts to your desktop and open it with any text editor.
6. The next step is to add the ip address of your phone[One you would usally ssh with] under the localssh text like this 
7. ![ss1](ss1.png)
8. Now save X0.hosts and copy it back to your xming folder to replace it with the regular X0.hosts folder.
9. Make sure you have both openjdk-16-jre and openjdk-jre from your package manager and also fontconfig and also fontconfig-config. 
10. Find a way to obtain the IP adress of your pc. You can find it by typing ipconfig/all on cmd or following step 11. Make sure to keep note of that address.
11. Now go the bottom right of your screen and right click on the xming logo and click on view log. Search for the text XdmcpRegisterConnection: newAddress [shows your own adress]
12. Now ssh into your phone with ssh mobile@{ip of device] and type in your password when prompted.
13. Hover on the Xming logo on the bottom right and keep track of weather it says :0 or :0.0
14. Now go back to your ssh cli and type in export DISPLAY={ip of computer]:[number of 0 from above]. and it should look something like this export DISPLAY=192.168.131:0.0 with either 1 or 2 0
15. now confirm that it has entered correctly by typing in echo $DISPLAY and make sure it reads the display number from above. 
16. With your client jar file hopefully downloaded, follow the first step for creating the launcher_profiles.json from this page if you haven't. https://github.com/PojavLauncherTeam/PojavLauncher_iOS/wiki/Installing-Forge
17. Now type in the command java -jar [path to jar file] and you should now see the gui for the installer show up on your windows computer.
18. Before clicking anything, make sure to set the install path to the correct path: /var/mobile/Documents/minecraft/ instead of whatever it showed.

That should be it. 
