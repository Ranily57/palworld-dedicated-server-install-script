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

# 🚀 Server Control Commands

## 🛑 Shutdown Command
- **Command**: `/Shutdown {Seconds} {MessageText}`
- **Description**: Shuts down the server after the specified number of seconds. A message will be displayed to all players.
- **Usage**: `/Shutdown 60 Server restarting in 1 minute`

## 🛑 DoExit Command
- **Command**: `/DoExit`
- **Description**: Immediately forces the server to stop.

## 📣 Broadcast Command
- **Command**: `/Broadcast {MessageText}`
- **Description**: Sends a message to all players on the server.
- **Usage**: `/Broadcast Attention all players: maintenance starting soon.`

## 🦵 KickPlayer Command
- **Command**: `/KickPlayer {SteamID}`
- **Description**: Kicks a player from the server using their SteamID.
- **Usage**: `/KickPlayer 12345678901234567`

## 🚫 BanPlayer Command
- **Command**: `/BanPlayer {SteamID}`
- **Description**: Bans a player from the server using their SteamID.
- **Usage**: `/BanPlayer 12345678901234567`

## 🌐 TeleportToPlayer Command
- **Command**: `/TeleportToPlayer {SteamID}`
- **Description**: Teleports you to the current location of the target player.
- **Usage**: `/TeleportToPlayer 12345678901234567`

## 🎯 TeleportToMe Command
- **Command**: `/TeleportToMe {SteamID}`
- **Description**: Teleports the target player to your current location.
- **Usage**: `/TeleportToMe 12345678901234567`

## 👥 ShowPlayers Command
- **Command**: `/ShowPlayers`
- **Description**: Displays information on all connected players.

## ℹ️ Info Command
- **Command**: `/Info`
- **Description**: Shows server information.

## 💾 Save Command
- **Command**: `/Save`
- **Description**: Saves the world data.
