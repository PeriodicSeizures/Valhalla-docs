# Reference

Valhalla utilizes Lua to take advantage of many of the available 
internal features. This is made possible with the sol Lua wrapper 
library. 

## API Reference format

### Accessor
    
The word *accessor* when used in this documentation will 
represent either methods or fields. A method is an accessor but 
not all accessors are methods. The same thing goes for fields, 
which will sometimes be referred to as properties.

### Uppercase .

API References which start in uppercase (i.e. `Vector2i.new()`, `ZDOID.NONE`)
generally belong to a class.

### Lowercase . :
  
API References which start in lowercase (i.e. `vector3.y`, `vector3:Distance(other)`)
generally belong to a instantiated class object.

### Parameter naming

| Name              | Assumed type
| :----------       | :---------- 
| target/uuid/owner | Int64
| somethingHash     | number (value within int32_t)
| other             | same class type
| bytes             | Bytes
| container<~>    | sol container of specified types
| strings           | container<string\>
