# Valhalla dedicated server

## Overview

Valhalla is an implementation of the Valheim dedicated server written in C++.
Valhalla not only includes but expands on the Valheim server
config. Some settings that are included are ZDO 
send rates, world-generation, spawning and more. 

## World

World loading is fully supported with an optional legacy mode
to support loading very old worlds. Saving is also fully functional with 
customizeable save times and compressed rolling backups.

## Logging

Logging can be in color, have
verbosity set per module, and other settings 
(see [easylogging++](https://github.com/amrayn/easyloggingpp#vmodule)).

Examples of command line arguments: 

  > Starts server with verbosity of Resource module set to 1
  ```
  .\Valhalla.exe -vmodule=VUtilsResource=1
  ```
  
  > Starts server with colors disabled and verbosity of Peer and PrefabModules set to 2 (notice the quotes)
  ```
  .\Valhalla.exe --no-colors "-vmodule=Peer=2,PrefabManager=2"
  ```
  
  > Starts server without backing up the last log and global verbosity set to 2
  ```
  .\Valhalla.exe --no-log-backup --v=2
  ```

  > Starts server with full verbosity enabled (spammy console)
  ```
  .\Valhalla.exe -v
  ```

Log files are backed up during restarts.

## Lua API

Valhalla includes a feature-rich Lua API to manipulate the inner-workings 
of the server. See the [API reference](reference/) for more details and 
documentation.

Several already-created mods are included with Valhalla to serve as 
examples and demonstrations of what is possible with the API.

Several of these implement core functionality of Valheim but can be
removed. Note that this might affect sleeping and/or portals.

An implementation of the BetterNetworking mod exists to support
compatible mod. It fully supports
compression and the other mod-specific settings (like send rates) 
are already built into the server config.