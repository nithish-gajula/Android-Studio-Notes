# Android-Studio-Info


#### Visual Studio Code Shortcuts Keys
- To preview the `Readme.md` file in VSCode -> `Ctrl + Shift + V`
- To format the json document in VSCode -> `Ctrl + K` then `Ctrl + F`
- To format any document, install and then set the **Prettier** extension as the default formatter using `Ctrl + Shift + P`,  
  then format file -> `Shift + Alt + F`
- To see difference between two files `code --diff file1.txt file2.txt` 

#### Android Studio Shortcuts Keys
- **Reformat** the code in Android Studio -> `Ctrl + Alt + L`
- **Expand** all code blocks in Android Studio -> `Ctrl + Shift + +`
- **Collapse** all code blocks in Android Studio -> `Ctrl + Shift + -`

### Missing Vector Asset Icons
- **Fix** it by deleting the **icons_metadata.txt** file
- Goto Android Studio -> File -> Settings -> Search 'Android SDK' -> there you can see 'Android SDK Location', note it (Example path for Linux: /root/Android/Sdk)
- Delete the icons_metadata.txt file from this path -> **/root/Android/Sdk/icons/material/icons_metadata.txt**

#### Emulator commands
`adb emu kill`  
`~/Android/Sdk/emulator/emulator -list-avds`  
`~/Android/Sdk/emulator/emulator -avd Small_Phone`  
`~/Android/Sdk/emulator/emulator -avd Medium_Phone_API_36.0`  
`adb pair 192.168.1.99:44641`  
`Enter pairing code`  
`adb pair 192.168.1.99:44641`  


###### To transfer files from desktop to android using termux app
##### In Android:
Download Termux App from Playstore  
`pkg update`  
`pkg install openssh`  
`passwd` - to set a password for ssh  
`sshd` - to start the ssh service  
`ifconfig` (wlan0) - note the ip  
`whoami` - to find the username  
tmux port = 8022  
`pwd` - to know the present working directory (termux home directory)  
`mv ~/file.txt /sdcard/Download/`  

##### In Linux Desktop :
`ping 192.168.1.99` (Android mobile IP)  
`scp -P 8022 /home/icps1101/Downloads/file.txt u0_a369@192.168.1.99:/data/data/com.termux/files/home/`  
`scp -P 8022 /home/icps1101/Downloads/file2.txt u0_a369@192.168.1.99:/sdcard/Download/`  
`ssh u0_a369@192.168.1.99 -p 8022`  

#### Wireless Debugging Procedure :

- Connect Mobile to 'ICPS 3FL 5GHz' wifi
- Make sure adb is installed on the desktop using the 'adb version' command
- Developer Options -> Wireless Debugging -> Enable -> Pair device with pairing code -> Note the IP, Port, and Pairing Code (changes every time)
- type command in desktop in **sudo**, ===> `adb pair IP_ADDRESS:PORT`
- It asks for a pairing code. Enter pairing code
- If success, then type ===> `adb connect IP_ADDRESS:PORT`
- adb devices, you can see the connected devices
- Android Studio automatically detects it.

Arial Black
Dialog
Fira Code
Fira Code Medium
HP Simplified
Inter
Inter Semi Bold
Microsoft Sans Serif
Nirmal UI
SansSerif
Verdana



### Duplicating a project
```
cd /home/icps1101/Downloads/projects
cp -r "EasyMarkdown" "TestingMarkdown"
```

Step 2 – Open the Duplicate in Android Studio
In Android Studio:
**File → Open… → Select TestingMarkdown**
Wait for Gradle sync to complete.

Step 3 – Change the Application Name (UI label)
Open: app/src/main/res/values/strings.xml
Edit
```<string name="app_name">Easy Markdown</string>```
Change to:
```<string name="app_name">Testing Markdown</string>```


In the Project view (set to Android mode), expand:

```app/java/com/example/easymarkdown```
Right-click on ```easymarkdown → Refactor → Rename → type testingmarkdown.```

Android Studio will ask if you want to search in comments/strings — check it.

After renaming, open app/build.gradle and update applicationId to match the new package path:

applicationId "com.nithishgajula.testingmarkdown"




<font color='yellow'>**TODO**</font>


## GitHub Commands
### Merge
- First, switch to master: `git checkout master`  
- Pull latest changes (if working with remote): `git pull origin master`  
- Merge your feature branch into master: `git merge update-to-targetSdk-35`  
- If no conflicts, the commit completes automatically. Otherwise, resolve conflicts manually.
- Push updated master to GitHub: `git push origin master`  


## Password Reset Procedures
### Windows
If you forgot the Windows login password. You can reset the password without losing the data

Be on the lock screen of Windows
Hold down the Shift Key and go to power icon and click restart (keep holding the shiftkey until system restarts and directly go to the BIOS blue screen)
There you go to the Troubleshoot > Advanced options > Command Prompt

Type `C:`  
Type `cd windows\system32`  
Type `ren utilman.exe utilman.exe.bak` (This backs up the Accessibility icon utility)  
Type `copy cmd.exe utilman.exe` (This replaces that icon with the Command prompt)  
Type `wpeutil reboot` (This will restart the computer)  


When you reach the Windows login screen, click the Accessibility icon to open the command prompt  
Type `net user "USER_NAME" NEW_PASSWORD` (Here replace the USER_NAME with original username and NEW_PASSWORD with new password that you want to keep, minimum 4 digits)  
Now close the command prompt and try to log-in with your new password.  
