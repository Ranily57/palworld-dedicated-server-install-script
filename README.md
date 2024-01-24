# palworld-dedicated-server-install-script
This repo is for the install script of Palworld, you can make PR if you see some change to do 

You'll have the install script on the repo if needed, if you have this issue: 

```sh
.steam/sdk64/steamclient.so: cannot open shared object file: No such file or directory
```
you'll need to execute the following command: 

```sh
mkdir -p ~/.steam/sdk64/
steamcmd +login anonymous +app_update 1007 +quit
cp ~/Steam/steamapps/common/Steamworks\ SDK\ Redist/linux64/steamclient.so ~/.steam/sdk64/
```

When the server start, if the `steamclient.so` is Ok, we don't need to take care of the rest of the error if the server start correctly. 
