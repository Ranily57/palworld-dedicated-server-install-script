# palworld-dedicated-server-install-script
This repo is for the install script of Palworld, you can make PR if you see some change to do 

## Windows 

to execute correctly the .Bat script for Windows, please ensure to have [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD#Windows) installed and ready to use.

When it's done, drop the .bat script into the steamcmd folder and execute it. 

## Linux 

To execute correctly the .sh script for Linux (Ubuntu, Debian), please ensure to have installed SteamCMD with the following command : 
```sh
sudo apt install steamcmd
``` 

When it's done, execute the .sh script anywhere on your server to start the install.

## Error

You'll have the install script on the repo if needed, if you have this issue: 

```sh
.steam/sdk64/steamclient.so: cannot open shared object file: No such file or directory
```
you'll need to execute the following command (Linux only): 

```sh
mkdir -p ~/.steam/sdk64/
steamcmd +login anonymous +app_update 1007 +quit
cp ~/Steam/steamapps/common/Steamworks\ SDK\ Redist/linux64/steamclient.so ~/.steam/sdk64/
```

When the server start, if the `steamclient.so` is Ok, we don't need to take care of the rest of the error if the server start correctly. 
