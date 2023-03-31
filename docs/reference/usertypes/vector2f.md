# Vector2f

A vector consisting of two floating point components

### `Vector2f.new()`
  > Returns `Vector2`

  > Constructs a Vector2 equivalent to Vector2.ZERO

### `Vector2f.new(x, y, z)`
  > Returns `Vector2`

  > Constructs a Vector2 from x, y, and z parameters

### `Vector2f.ZERO`
  > Returns `Vector2` | **readonly**
  
  > A zero vector (0, 0)

### `vector2f.x`
  > Returns `number`

  > The x component of the vector

### `vector2f.y`
  > Returns `number`

  > The y component of the vector

### `vector2f.magnitude`
  > Result: `number` | **readonly**

  > The length of the vector
  
### `vector2f.sqMagnitude`
  > Result: `number` | **readonly**

  > The squared length of the vector

### `vector2f.normal`
  > Result: `Vector2f` | **readonly**
  
  > Returns the unit normal vector of this

### `vector2f:Distance(other)`
  > Returns `number`

  > The distance another vector and this

### `vector2f:SqDistance(other)`
  > Result: `number`

  > The squared distance another vector and this

### `vector2f:__add()`
  > Returns `Vector2`

  > Adds together two vectors
  
  > 
  ```lua
  local a = Vector2.new(1, 5)
  local b = Vector2.new(2, -1)
  
  -- (3, 4)
  local result = a + b
  ```

### `vector2f:__sub()`
  > Returns `Vector2`

  > Subtracts two vectors
  
  > 
  ```lua
  local a = Vector2.new(6, -1)
  local b = Vector2.new(-3, -2)
  
  -- (9, 1)
  local result = a - b
  ```
  
### `vector2f:__mul()`
  > Returns `Vector2`

  > Multiplies two vectors
  
  > 
  ```lua
  local a = Vector2.new(1, 2)
  local b = Vector2.new(4, 5)
  
  -- (4, 10)
  local result = a * b
  ```

### `vector2f:__div()`
  > Returns `Vector2`

  > Divides two vectors

  > 
  ```lua
  local a = Vector2.new(6, 4)
  local b = Vector2.new(3, 2)
  
  -- (2, 2)
  local result = a / b
  ```