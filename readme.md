# How to install the Sitecore theme

This guide exists of 3 steps:

1) Copy the required resources
2) Update the profiles.json with the correct settings
3) Update the Powershell prompt with the dracula theme

a big callout to Jason 'Taco' Wilkerson for creating this cool background!

## 1 - copy resources to the Windows terminal folder

copy the contents of the "src" folder to the windows terminal rootfolder. Just copy the location in the code snippet below and paste it in your windows explorer

```
%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState
```

## 2 - update your profiles.json

Update profiles.json with the correct settings. the first action is to add the theme to the profiles array. The file can be found in the same location as where the theme was copied. Just copy the code below and vs code will be opened to edit the profile.

```
code %LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState\profiles.json
```

copy the snippet below and paste it at the end of the profiles array. Please note that it doesn't differ that much from the original theme. I chose to use the default theme, update the icon and the background and use a powershell script to update to the dracula theme

```json
,
{
    "acrylicOpacity" : 0.5,
    "backgroundImage" : "ms-appdata:///roaming/sitecore-theme/Sitecore-Dark2.png",
    "backgroundImageOpacity" : 0.80000001192092896,
    "backgroundImageStretchMode" : "uniformToFill",
    "closeOnExit" : true,
    "colorScheme" : "Campbell",
    "commandline" : "powershell.exe",
    "cursorColor" : "#FFFFFF",
    "cursorShape" : "bar",
    "fontFace" : "Consolas",
    "fontSize" : 10,
    "guid" : "{0caa0dad-35be-5f56-a8ff-afceeeaa6102}",
    "historySize" : 9001,
    "icon" : "ms-appdata:///roaming/sitecore-theme/sitecore-icon.png",
    "name" : "Sitecore",
    "padding" : "0, 0, 0, 0",
    "snapOnInput" : true,
    "startingDirectory" : "%USERPROFILE%",
    "useAcrylic" : false
}
```