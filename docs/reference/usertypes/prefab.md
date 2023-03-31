# Prefab

### `prefab.name`
  > Returns `string` | **Readonly**
  
### `prefab.hash`
  > Returns `number` | **Readonly**

### `prefab:AnyFlagsPresent(flags)`
  > Returns `boolean`
  
  > Whether all of th especified flags are present on this prefab
  
### `prefab:AnyFlagsPresent(flags)`
  > Whether any of the specified flags are present on this prefab
  
  > 
  ```lua
  local prefab = zdo.prefab
  
  if prefab:AnyFlagsPresent(Flag.BED | Flag.DOOR) then
      -- will run if object is a bed or door
  end
  ```

### `prefab:AllFlagsAbsent(flags)`
  > Whether all the specified flags are absent on this prefab
  
  > 
  ```lua
  local prefab = zdo.prefab
  
  -- the same as 'not prefab:AllFlagsPresent(Flag.SESSIONED)'
  if prefab:AllFlagsAbsent(Flag.SESSIONED) then
      -- will run if object is persistent
  end  
  ```

### `prefab:AnyFlagsAbsent(flags)`
  > Returns `boolean`
  
  > Whether any of the specified flags are absent from the prefab
  
