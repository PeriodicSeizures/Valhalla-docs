# Vector2i

A vector consisting of two integer components

### `Vector2i.new()`
  > Returns `Vector2i`

  > Constructs a Vector2i equivalent to Vector2i.ZERO

### `Vector2i.new(x, y, z)`
  > Returns `Vector2i`

  > Constructs a Vector2i from x, y, and z parameters

### `Vector2i.ZERO`
  > Returns `Vector2i`
  
  > A zero vector (0, 0)

### `vector2i.x`
  > Returns `number`

  > The x component of the vector

### `vector2i.y`
  > Returns `number`

  > The y component of the vector

### `vector2i.magnitude`
  > Result: `number` | readonly

  > The length of the vector
  
### `vector2i.magnitude`
  > Result: `number` | readonly

  > The squared length of the vector

### `vector2i.normalized`
  > Result: `Vector2i` | readonly

  > A vector with a length of one and same direction as this

### `vector2i:Distance(other)`
  > Returns `number`

  > The distance another vector and this

### `vector2i:Normalize()`
  > Result: `Vector2i&`
  
  > *Note: using an temporary reference might break things*

  > Normalizes the vector and return this

### `vector2i:SqDistance(other)`
  > Result: `number`

  > The squared distance another vector and this

### `vector2i:__add()`
  > Returns `Vector2i`

  > Adds together two vectors
  
  > 
  ```lua
  local a = Vector2i.new(1, 5)
  local b = Vector2i.new(2, -1)
  
  -- (3, 4)
  local result = a + b
  ```

### `vector2i:__sub()`
  > Returns `Vector2i`

  > Subtracts two vectors
  
  > 
  ```lua
  local a = Vector2i.new(6, -1)
  local b = Vector2i.new(-3, -2)
  
  -- (9, 1)
  local result = a - b
  ```
  
### `vector2i:__mul()`
  > Returns `Vector2i`

  > Multiplies two vectors
  
  > 
  ```lua
  local a = Vector2i.new(1, 2)
  local b = Vector2i.new(4, 5)
  
  -- (4, 10)
  local result = a * b
  ```

### `vector2i:__div()`
  > Returns `Vector2i`

  > Divides two vectors

  > 
  ```lua
  local a = Vector2i.new(6, 4)
  local b = Vector2i.new(3, 2)
  
  -- (2, 2)
  local result = a / b
  ```