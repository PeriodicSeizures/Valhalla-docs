# Reference

Valhalla utilizes Lua to take advantage of many of the available 
internal features. This is made possible with the sol Lua wrapper 
library. 

See [the code](https://github.com/PeriodicSeizures/Valhalla/blob/fix-zdos/src/ModManager.cpp#L64)
for the actual implementation and stuff that might not
be fully included in this documentation

## API Reference format

### Accessor
    
The word *accessor* when used in this documentation will 
represent either methods or fields. A method is an accessor but 
not all accessors are methods. The same thing goes for fields, 
which will sometimes be referred to as properties.

### Uppercase

API References which start in uppercase (i.e. `Vector2i.new()`, `ZDOID.NONE`)
generally belong to a class.

### Lowercase
  
API References which start in lowercase (i.e. `vector3.y`, `vector3:Distance(other)`)
generally belong to a instantiated class object.

### Parameter naming

| Name              | Assumed type
| :----------       | :---------- 
| target/uuid/owner | Int64
| somethingHash     | number (value within int32_t)
| other             | same class type
| bytes             | Bytes
| container<~>      | sol container of specified types
| strings           | container<string\>
| zone              | Vector2i

### Danger zone

Some usertypes are unsafe to store for long periods or outside the
scope in which they are accessed from. These objects currently are:

    `Peer`     
    `ZDO`

`Peer` can be safely stored outside of any scope, but must be cleaned-up
accordingly when a player [disconnects](http://127.0.0.1:8000/reference/managers/valhalla/#valhallasubscribename-function)

`ZDO` currently has no mechanism or callback that is invoked to notify 
the mod of zdo deletion. An alternative to storing the ZDO would be
to use zdo.id (`ZDOID`), which are completely safe to store (unless otherwise stated).

Violating any of the above will result in hard-to-diagnose problems, 
weird stuff, or the moon falling out of orbit.