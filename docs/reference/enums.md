# Enums

Several labeled constants are used throughout Valhalla, and they are listed here
for easy reference.

They can be accessed by the name of the enum table and the enum itself:

  > `TimeOfDay.DAY`
  
  > `Flag.CHAIR`
  
### `Type`
  > | Type        | Alias
  > | :---------- | :-------
  > | BOOL        |
  > | STRING      | 
  > | STRINGS     |
  > | BYTES       |
  > | ZDOID       |
  > | VECTOR3     |
  > | VECTOR2i    |
  > | QUATERNION  |
  > | INT8        |
  > | INT16       | SHORT
  > | INT32       | INT, HASH
  > | INT64       | LONG
  > | UINT8       | BYTE
  > | UINT16      | USHORT
  > | UINT32      | UINT
  > | UINT64      | ULONG
  > | FLOAT       |
  > | DOUBLE      |
  > | CHAR        |
  
### `TimeOfDay`
  > | TimeOfDay   | Value      
  > | :---------- | :----------
  > | MORNING     | 240        
  > | DAY         | 270        
  > | AFTERNOON   | 900        
  > | NIGHT       | 1530       
  
### `ChatMsgType`
  > | ChatMsgType
  > | :----------
  > | WHISPER    
  > | NORMAL        
  > | SHOUT  
  > | PING

### `Flag`
  > Prefab flags which are to be masked together as bitmasks

  > | Flag          | Description
  > | :----------   | :----------
  > | NONE          | Default flag
  > | SCALE         | Send initial scale
  > | FAR           | Is an object visible from far away
  > | SESSIONED     | Temporary client-ZDO
  > | PIECE         | Is a player-buildable object
  > | BED           | Is a bed
  > | DOOR          | Is a door
  > | CHAIR         | Is a chair
  > | SHIP          | Is a sailable ship
  > | FISH          | Is a swimming fish
  > | PLANT         | Is a player-plantable crop
  > | ARMATURE      | Is an armorstand that hold items
  > | ITEM          | Is a dropped ground item
  > | PICKABLE      | Is a player-interactible object
  > | PICKABLE_ITEM | Is a pickable ground item
  > | COOKING       | Is a cooking station
  > | CRAFTING      | Is a crafting station
  > | SMELTING      | Is an ore-refining station
  > | BURNING       | Is a torch or other campfire type
  > | SUPPORT       | Is a supportable structure with strength
  > | BREAKABLE     | Is a destructible object capable of taking damage
  > | ATTACH        | Is a utility component that holds items in physical space
  > | ANIMAL        | Is a passive creature
  > | MONSTER       | Is a neutral or hostile creature
  > | TAME          | Is a tameable creature
  > | BREED         | Is a breedable creature
  > | MINEABLE_OLD  | Old class type useful only for leviathan
  > | MINEABLE      | Is a pickaxe-mineable object
  > | TREE          | Is an upright tree
  > | LOG           | Is a chopped down tree
  > | SFX           | Is a temporary sound object
  > | VFX           | Is a temporary visual effects object
  > | AOE           | Is a temporary attack object
  > | DUNGEON       | Is a dungeon object
  > | PLAYER        | Is a player character
  > | TOMBSTONE     | Is a player tombstone