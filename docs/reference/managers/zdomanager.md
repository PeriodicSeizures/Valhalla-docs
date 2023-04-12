# ZDOManager

Manager class for keeping client objects updated

!!! danger test
    Accessing ZDOs after they have been manually collected with `DestroyZDO` or automatically collected by a client **will** crash your program.
    
    Make sure to store ZDOs by their id instead of the ZDO itself.

I need better formatting ideas for this, ie how to organize overloads and stuff,

## ZDOManager:GetZDO(zdoid)
  > Returns `ZDO` or `nil`
  
## ZDOManager:SomeZDOs...
  > Returns `container<ZDO>`
  
  > Find up to `max` ZDOs
  
  > 
  ```lua title="Positional overloads"
  ZDOManager:SomeZDOs(pos, radius, max, pred)
  ZDOManager:SomeZDOs(pos, radius, max)
  ZDOManager:SomeZDOs(pos, radius, max, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:SomeZDOs(pos, radius, max, prefabName)
  ```
  
  >
  ```lua title="Get up to 5 ZDOs near any joining player within 16m"  hl_lines="2 2"
  Valhalla:Subscribe('Join', function(peer)
    local zdos = ZDOManager:SomeZDOs(peer.pos, 16, 5)
    
    -- do stuff with zdos...
  end)
  
  ```
  
  >
  ```
  ZDOManager:SomeZDOs(zone, max)
  ZDOManager:SomeZDOs(zone, max, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:SomeZDOs(zone, max, prefabName)
  ```
  
  >
  ```
  ZDOManager:SomeZDOs(zone, max, pos, radius, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:SomeZDOs(zone, max, pos, radius, prefabName)
  ```
  
### `ZDOManager:GetZDOs`
  > Returns `container<ZDO>`
  
  
  > Get all the ZDOs in world with optional specifiers:
  
  >  
  ```lua  
  ZDOManager:GetZDOs(prefabHash)
  
  ZDOManager:GetZDOs(prefabName)
  
  ZDOManager:GetZDOs(pos, radius, pred)
  
  ZDOManager:GetZDOs(pos, radius)
  ZDOManager:GetZDOs(pos, radius, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:GetZDOs(pos, radius, prefabName)
  
  ZDOManager:GetZDOs(zone, pred)
  
  ZDOManager:GetZDOs(zone)
  ZDOManager:GetZDOs(zone, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:GetZDOs(zone, prefabName)
  
  ZDOManager:GetZDOs(zone, pos, radius, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:GetZDOs(zone, pos, radius, prefabName)
  ```

### `ZDOManager:AnyZDO(pos, radius, prefabHash, flagsPresent, flagsAbsent)`
  > Returns `ZDO` or `nil`
  
  > Attempts to find any singular ZDO within a radius of position of prefab and flags
  
  >
  ```lua
  ZDOManager:AnyZDO(pos, radius, prefabName)
  ```
  
### `ZDOManager:AnyZDO(zone, prefabHash, flagsPresent, flagsAbsent)`
  > Returns `ZDO` or `nil`
  
  > Attempts to find any singular ZDO within a zone of prefab and flags
  
  >
  ```lua
  ZDOManager:AnyZDO(zone, prefabName)
  ```
  
### `ZDOManager:NearestZDO(pos, radius, func)`
  > Returns `ZDO` or `nil`
  
  > Attempts to find the nearest ZDO within a radius of position passing a binary predicate
  
  >
  ```lua
  ZDOManager:NearestZDO(pos, radius, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:NearestZDO(pos, radius, prefabName)
  ```
  
### `ZDOManager:ForceSendZDO(zdoid)`
  > Forcibly sends a ZDO to all clients, regardless of distance to peer or last revision time
  
### `ZDOManager:DestroyZDO(zdo)`
  > Destroys a ZDO on both the server side and on all clients
  
### `ZDOManager:Instantiate(prefab, pos, rot)`
  > Returns `ZDO`
  
  > Instantiates a new ZDO with prefab at position with rotation
  
  > Overloads which accept a prefab name or hash will throw if no prefab could be found
  
  >
  ```lua
  ZDOManager:Instantiate(prefab, pos)
  ZDOManager:Instantiate(prefabName, pos, rot)
  ZDOManager:Instantiate(prefabName, pos)
  ZDOManager:Instantiate(prefabHash, pos, rot)
  ZDOManager:Instantiate(prefabHash, pos)
  ZDOManager:Instantiate(zdo)
  ```