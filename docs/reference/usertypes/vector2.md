# Vector2

A vector consisting of two floating point components

### `Vector2.new()`
  > Returns `Vector2`

  > Constructs a Vector2 equivalent to Vector2.ZERO

### `Vector2.new(x, y, z)`
  > Returns `Vector2`

  > Constructs a Vector2 from x, y, and z parameters

### `Vector2.ZERO`
  > Returns `Vector2` | **readonly**
  
  > A zero vector (0, 0)

### `Vector2.x`
  > Returns `number`

  > The x component of the vector

### `Vector2.y`
  > Returns `number`

  > The y component of the vector

### `Vector2.magnitude`
  > Result: `number` | **readonly**

  > The length of the vector
  
### `Vector2.magnitude`
  > Result: `number` | **readonly**

  > The squared length of the vector

### `Vector2.normalized`
  > Result: `Vector2` | **readonly**

  > A vector with a length of one and same direction as this

### `Vector2:Distance(other)`
  > Returns `number`

  > The distance another vector and this

### `Vector2:Normalize()`
  > Result: `Vector2&`
  
  > *Note: using an temporary reference might break things*

  > Normalizes the vector and return this

### `Vector2:SqDistance(other)`
  > Result: `number`

  > The squared distance another vector and this

### `Vector2:__add()`
  > Returns `Vector2`

  > Adds together two vectors
  
  > 
  ```lua
  local a = Vector2.new(1, 5)
  local b = Vector2.new(2, -1)
  
  -- (3, 4)
  local result = a + b
  ```

### `Vector2:__sub()`
  > Returns `Vector2`

  > Subtracts two vectors
  
  > 
  ```lua
  local a = Vector2.new(6, -1)
  local b = Vector2.new(-3, -2)
  
  -- (9, 1)
  local result = a - b
  ```
  
### `Vector2:__mul()`
  > Returns `Vector2`

  > Multiplies two vectors
  
  > 
  ```lua
  local a = Vector2.new(1, 2)
  local b = Vector2.new(4, 5)
  
  -- (4, 10)
  local result = a * b
  ```

### `Vector2:__div()`
  > Returns `Vector2`

  > Divides two vectors

  > 
  ```lua
  local a = Vector2.new(6, 4)
  local b = Vector2.new(3, 2)
  
  -- (2, 2)
  local result = a / b
  ```