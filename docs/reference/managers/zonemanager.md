# ZoneManager

Manager class for all things related to world generation.

*Note: Zone / zone is a typedef for Vector2i and can be considered the same thing*

### `ZoneManager:GenerateZone(zone)`
  > Forcibly generates a zone in world
  
  > Will spawn all new features and vegetation with no deletion

### `ZoneManager:GetNearestFeature(name, pos)`
  > Returns `FeatureInstance` or `nil`
  
  > Finds the nearest Feature to position with name 
  
### `ZoneManager:WorldToZonePos(pos)`
  > Returns `Zone`
  
  > Converts from world coordinates to zone coordinates
  
### `ZoneManager:ZoneToWorldPos(zone)`
  > Returns `Vector3`
  
  > Converts from zone coordinates to world coordinates
  
### `ZoneManager.globalKeys`
  > Returns `container<string>`
  
  > The currently active global keys. 
  See [Global keys](https://valheim.fandom.com/wiki/Global_Keys)
  for more information.