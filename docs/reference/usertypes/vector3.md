# Vector3

A vector consisting of three floating point components

### `Vector3.new()`
  > Returns `Vector3`

  > Constructs a Vector3 equivalent to Vector3.ZERO

### `Vector3.new(x, y, z)`
  > Returns `Vector3`

  > Constructs a Vector3 from x, y, and z parameters

### `Vector3.ZERO`
  > Returns `Vector3`
  
  > A zero vector (0, 0, 0)

### `vector3.x`
  > Returns `number`

  > The x component of the vector

### `vector3.y`
  > Returns `number`

  > The y component of the vector

### `vector3.z`
  > Returns `number`

  > The z component of the vector
  
### `vector3.magnitude`
  > Returns `number` | readonly

  > The length of the vector
  
### `vector3.sqMagnitude`
  > Returns `number` | readonly

  > The squared length of the vector
  
### `vector3.normalized`
  > Returns `Vector3` | readonly

  > A vector with a length of one and same direction as this

### `vector3:Distance(other)`
  > Returns `number`

  > The distance another vector and this

### `vector3:Normalize()`
  > Returns `Vector3&`
  
  > *Note: using an temporary reference might break things*

  > Normalizes the vector and return this

### `vector3:SqDistance(other)`
  > Returns `number`

  > The squared distance another vector and this

### `vector3:__add()`
  > Returns `Vector3`

  > Adds together two vectors
  
  > 
  ```lua
  local a = Vector3.new(1, 0.5, 1)
  local b = Vector3.new(2, -1, -2)
  
  -- (3, -0.5, -1)
  local result = a + b
  ```

### `vector3:__sub()`
  > Returns `Vector3`

  > Subtracts two vectors

  > 
  ```lua
  local a = Vector3.new(6, -2.3, -4)
  local b = Vector3.new(-3, -2, 2)
  
  -- (9, -0.3, -6)
  local result = a - b
  ```

### `vector3:__mul()`
  > Returns `Vector3`

  > Multiplies two vectors
  
  > 
  ```lua
  local a = Vector3.new(1, 2, 3)
  local b = Vector3.new(4, 5, 6)
  
  -- (4, 10, 18)
  local result = a * b
  ```

### `vector3:__div()`
  > Returns `Vector3`

  > Divides two vectors

  > 
  ```lua
  local a = Vector3.new(6, 4, 10)
  local b = Vector3.new(3, 2, 2)
  
  -- (2, 2, 5)
  local result = a / b
  ```
