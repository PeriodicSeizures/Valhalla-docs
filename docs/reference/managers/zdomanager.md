# ZDOManager

Manager class for keeping client objects updated

### `ZDOManager:GetZDO(zdoid)`
  > Returns `ZDO` or `nil`
  
### `ZDOManager:SomeZDOs(pos, radius, max, func)`
  > Returns `container<ZDO>`
  
  > Find up to `max` ZDOs within a radius of position that pass a binary predicate
  
  > `ZDOManager:SomeZDOs(vec, 20, 10, function(zdo) return true end)`
  
  >
  ```lua
  ZDOManager:SomeZDOs(pos, radius, max)
  ZDOManager:SomeZDOs(pos, radius, max, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:SomeZDOs(pos, radius, max, prefabName)
  ```
  
### `ZDOManager:SomeZDOs(zone, max, func)`
  > Returns `container<ZDO>`
  
  > Find up to `max` ZDOs within a zone that pass a binary predicate
  
  >
  ```lua
  ZDOManager:SomeZDOs(zone, max)
  ZDOManager:SomeZDOs(zone, max, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:SomeZDOs(zone, max, prefabName)
  ```
  
### `ZDOManager:SomeZDOs(zone, max, pos, radius)`
  > Returns `container<ZDO>`
  
  > Find up to `max` ZDOs within a zone, then within a radius of position.

  >
  ```lua
  ZDOManager:SomeZDOs(zone, max, pos, radius, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:SomeZDOs(zone, max, pos, radius, prefabName)
  ```
  
### `ZDOManager:GetZDOs(prefabHash)`
  > Returns `container<ZDO>`
  
  > Get all the ZDOs in world of prefabHash
  
### `ZDOManager:GetZDOs(prefabName)`
  > Returns `container<ZDO>`
  
  > Get all the ZDOs in world of prefabName
  
### `ZDOManager:GetZDOs(pos, radius, func)`
  > Returns `container<ZDO>`
  
  > Find all ZDOs within a radius of position passing a binary predicate
  
  >  
  ```lua  
  ZDOManager:GetZDOs(pos, radius)
  ZDOManager:GetZDOs(pos, radius, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:GetZDOs(pos, radius, prefabName)
  ```
  
### `ZDOManager:GetZDOs(zone, func)`
  > Returns `container<ZDO>`

  > 
  ```lua
  ZDOManager:GetZDOs(zone)
  ZDOManager:GetZDOs(zone, prefabHash, flagsPresent, flagsAbsent)
  ZDOManager:GetZDOs(zone, prefabName)
  ```
  
### `ZDOManager:GetZDOs(zone, pos, radius)`
  > Returns `container<ZDO>`
  
  >
  ```lua
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