# Android-Studio-Info



#### Visual Studio Code Shortcuts Keys
- To preview the `Readme.md` file in VSCode -> `Ctrl + Shift + V`
- To format the json document in VSCode -> `Ctrl + K` then `Ctrl + F`
- To format any document, install and then set the **Prettier** extension as the default formatter using `Ctrl + Shift + P`,  
  then format file -> `Shift + Alt + F`

#### Android Studio Shortcuts Keys
- **Reformat** the code in Android Studio -> `Ctrl + Alt + L`
- **Expand** all code blocks in Android Studio -> `Ctrl + Shift + +`
- **Collapse** all code blocks in Android Studio -> `Ctrl + Shift + -`

#### Wireless Debugging Procedure :

- Connect Mobile to 'ICPS 3FL 5GHz' wifi
- Make sure adb is installed on the desktop using the 'adb version' command
- Developer Options -> Wireless Debugging -> Enable -> Pair device with pairing code -> Note the IP, Port, and Pairing Code (changes every time)
- type command in desktop in *sudo* : adb pair <IP>:<Port>
- It asks for a pairing code. Enter pairing code
- If success, then type: adb connect <IP>:<Port>
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