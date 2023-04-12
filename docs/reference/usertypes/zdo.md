# ZDO

The bread-and-butter of Valhiem

This class represents automatically synchronized networked objects 
and states throughout Valheim gameplay. 

### `zdo.id`
  > Returns `ZDOID` | **readonly**
  
  > The id of the zdo
  
### `zdo.pos`
  > Returns `Vector3f`
  
  > The position of the zdo
  
### `zdo.zone`
  > Returns `Vector2i` | **readonly**
  
  > The current zone the zdo is contained within
  
### `zdo.rot` 
  > Returns `Quaternion`
  
  > The rotation of the zdo
  
### `zdo.prefab`
  > Returns `Prefab`
  
### `zdo.owner`
  > Returns `Int64`
  
### `zdo:IsOwner(uuid)`
  > Returns `boolean`
  
  > Checks whether the specified uuid is the owner of the zdo
  
### `zdo:IsLocal`
  > Returns `boolean`
  
  > Whether the zdo is owned by the server
  
### `zdo:SetLocal`
  > Set the server as the owner of the ZDO
    
### `zdo:HasOwner()`
  > Returns `boolean`
  
  > Returns whether this zdo has an owner
  
### `zdo:Disown()`
  > Sets the zdo's owner to 0
  
### `zdo.dataRev`
  > Returns the zdo's data revision number
  
### `zdo.ownerRev`
  > Returns the zdo's owner revision number
  
### `zdo.ticksCreated`
  > Returns the time in ticks the zdo was created
  
## Get / Set

  > A zdo has several named getter and setter types
  
  > `GetFloat`, `GetInt`, `GetLong`, `GetQuaternion`, `GetString`, 
  `GetBytes`, `GetBool`, `GetZDOID`
  ```lua
  zdo:Get<>(hash, default)
  zdo:Get<>(hash)
  zdo:Get<>(name, default)
  zdo:Get<>(name)
  ```
  
  > `SetFloat`, `SetInt`, `Set`
  ```lua
  zdo:Set<>(hash, value)
  zdo:Set<>(name, value)  
  ```
  
  > The overload `Set(...)` accepts any of the above non-numeric types

  > Any usage of a long (64-bit integer) utilizes a `Int64` and is overloaded
    by `Set(...)`