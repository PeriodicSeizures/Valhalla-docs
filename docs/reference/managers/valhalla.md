# Valhalla

### `Valhalla.version`
  > Returns `string`

  > Valheim version: `0.214.300`
  
### `Valhalla.delta`
  > Returns `number`
  
  > The delta time for this frame
  
  > Equivalent to Unity `Time.deltaTime`
  
### `Valhalla.id`
  > Returns `number`

  > The randomly generated server id.

  > Used primarily for determining ZDO
  ownership throughout gameplay.
  
### `Valhalla.nanos`
  > Returns `number`

  > The time in nanoseconds
  
### `Valhalla.time`
  > Returns `number`
  
  > The time in seconds
  
  > Equivalent to Unity `Time.time`

### `Valhalla.worldTime`
  > Returns `number`

  > The in-game time which determines the day/night cycle

### `Valhalla.worldTimeMultiplier`
  > Returns `number`

  > The rate at which the worldTime advances. Setting to a value less than 1 will slow the rate 
  (might have weird client time-skip effects). Setting to a values greater than 1 will speed up the ingame time.
  
  > A simple use-case of this is the ingame-sleep time skip, which rapidly progresses the time until morning. See the 
  [Sleep mod](https://github.com/PeriodicSeizures/Valhalla/blob/f89bdaf3f34826576ba9befb6a74a934ed4f3e88/data/mods/Sleep/Sleep.lua#L77)
  for more information regarding usages.

### `Valhalla.worldTicks`
  > Returns `number`

  > Similar to worldTime but in C# `DateTime.Ticks`

### `Valhalla.day`
  > Returns `number`
  
  > The current integer day

### `Valhalla.timeOfDay`
  > Returns `number`
  
  > The current relative time of day. In Valheim, an entire cycle is 1800s, with day starting at a skewed 270s.
  This returns the time wrapped around 1800 (worldTime % 1800).

### `Valhalla.isMorning`
  > Returns `boolean`
  
  > Whether the current time is morning

### `Valhalla.isDay`
  > Returns `boolean`

  > Whether the current time is day

### `Valhalla.isAfternoon`
  > Returns `boolean`
  
  > Whether the current time is the afternoon

### `Valhalla.isNight`
  > Returns `boolean`
  
  > Whether the current time is night

### `Valhalla.tomorrowMorning`
  > Returns `number`
  
  > The worldTime for the morning time pertaining to the current `day` + 1

### `Valhalla.tomorrow`
> Returns `number`

  > The worldTime for the day time pertaining to the current `day` + 1

### `Valhalla.tomorrowAfternoon`
> Returns `number`

  > The worldTime for the afternoon time pertaining to the current `day` + 1

### `Valhalla.tomorrowNight`
> Returns `number`

  > The worldTime for the night time pertaining to the current `day` + 1

### `Valhalla:Subscribe(name, function)`
  > Subscribe to a game event
  
  > The passed function will be called when the event fires
  
  >
  ```lua
  Valhalla:Subscribe('Enable', function()
    -- Will be dispatched only once when all plugins are loaded
  end)
  
  Valhalla:Subscribe('RouteInAll', 'ChatMessage', function(peer, targetZdoid, bytes)
    -- Will be dispatched whenever a peer calls RoutedRpc that is aimed towards all online peers
  end)
  ```
  
  > Available event handlers:
  
  > | Method            | Dispatched                                                                                                        | Passthrough                           | Example                                                                                       |
  > | :----------       | :------------------                                                                                               | :---------------:                     | :-------                                                                                      |
  > | `Enable`          | Server start                                                                                                      | :material-close:                      | `Valhalla:Subscribe('Enable', function() end)`                                                |
  > | `Disable`         | Server stop                                                                                                       | :material-close:                      | `Valhalla:Subscribe('Disable', function() end)`                                               |
  > | `Update`          | Server update loop                                                                                                | :material-close:                      | `Valhalla:Subscribe('Update', function() end)`                                                |
  > | `Periodic`        | Once every second                                                                                                 | :material-close:                      | `Valhalla:Subscribe('Periodic', function() end)`                                              |
  > | `Connect`         | Any peer connects                                                                                                 | `Peer`                                | `Valhalla:Subscribe('Connect', function(peer) end)`                                           |
  > | `Disconnect`      | Any peer disconnects                                                                                              | `Peer`                                | `Valhalla:Subscribe('Disconnect', function(peer) end)`                                        |
  > | `Join`            | Valid peer joins                                                                                                  | `Peer`                                | `Valhalla:Subscribe('Join', function(peer) end)`                                              |
  > | `Quit`            | Valid peer quits                                                                                                  | `Peer`                                | `Valhalla:Subscribe('Quit', function(peer) end)`                                              |
  > | `RpcIn`           | :material-monitor: :material-arrow-right: :material-server:                                                       | `Peer`, `...`                         | `Valhalla:Subscribe('RpcIn', 'PeerInfo', function(peer, bytes) end)`                          |
  > | `RpcOut`          | :material-server: :material-arrow-right: :material-monitor:                                                       | `Peer`, `...`                         | `Valhalla:Subscribe('RpcOut', 'PeerInfo', function(peer, bytes) end)`                         |
  > | `RouteIn`         | :material-monitor: :material-arrow-right: :material-server:                                                       | `Peer`, `ZDOID`, `...`                | `Valhalla:Subscribe('RouteIn', 'SetGlobalKey', function(peer, zdoid, key) end)`               |  
  > | `RouteInAll`      | :material-monitor: :material-arrow-right: :material-server: :material-arrow-right: :material-monitor-multiple:    | `Peer`, `ZDOID`, `...`                | `Valhalla:Subscribe('RouteInAll', 'DestroyZDO', function(peer, zdoid, bytes) end)`            |  
  > | `RouteOut`        | :material-server: :material-arrow-right: :material-monitor:                                                       | `Peer`, `ZDOID`, `...`                | `Valhalla:Subscribe('RouteOut', 'SleepStart', function(peer, zdoid) end)`                     |  
  > | `RouteOutAll`     | :material-server: :material-arrow-right: :material-monitor-multiple:                                              | `ZDOID`, `...`                        | `Valhalla:Subscribe('RouteOutAll', 'GlobalKeys', function(zdoid, keys) end)`                  |  
  > | `Routed`          | :material-monitor: :material-arrow-right: :material-server: :material-arrow-right: :material-monitor:             | `Peer-src` `Peer-dst`, `ZDOID`, `...` | `Valhalla:Subscribe('RouteOutAll', 'AddItem', function(srcpeer, dstpeer, zdoid, item) end)`   |  
  > | `Send`            | Server sends packet                                                                                               | `Socket`, `Bytes`                     | `Valhalla:Subscribe('Send', function(socket, bytes) end)`                                     |  
  > | `Recv`            | Server receives packet                                                                                            | `Socket`, `Bytes`                     | `Valhalla:Subscribe('Recv', function(socket, bytes) end)`                                     |  
  > | `POST`            | Event-modifier to run after the primary-event
  
  > Most of the events above are prefix methods like in Harmony. Similarly, there is a `POST` event that can be 
  called after the major event has taken place. This only applies to `Rpc<>` and `Route<>` events 
  (maybe also to some others not listed here).
  
  >
  ```lua
  -- Will be ran after the internal PeerInfo has taken place
  Valhalla:Subscribe('RpcIn', 'PeerInfo' 'POST', function(peer, bytes) end)
  ```
  
  > Handlers using `POST` cannot be cancelled unless otherwise stated (because what would be cancelled after everything has already happened?).