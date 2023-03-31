# Vector3f

A vector consisting of three floating point components

### `Vector3f.new()`
  > Returns `Vector3f`

  > Constructs a Vector3f equivalent to Vector3f.ZERO

### `Vector3f.new(x, y, z)`
  > Returns `Vector3f`

  > Constructs a Vector3f from x, y, and z parameters

### `Vector3f.ZERO`
  > Returns `Vector3f`
  
  > A zero vector (0, 0, 0)

### `vector3f.x`
  > Returns `number`

  > The x component of the vector

### `vector3f.y`
  > Returns `number`

  > The y component of the vector

### `vector3f.z`
  > Returns `number`

  > The z component of the vector
  
### `vector3f.magnitude`
  > Returns `number` | **readonly**

  > The length of the vector
  
### `vector3f.sqMagnitude`
  > Returns `number` | **readonly**

  > The squared length of the vector

### `vector3f.normal`
  > Result: `Vector3f` | **readonly**
  
  > Returns the unit normal vector of this

### `vector3f:Distance(other)`
  > Returns `number`

  > The distance another vector and this

### `vector3f:SqDistance(other)`
  > Returns `number`

  > The squared distance another vector and this

### `vector3f:__add()`
  > Returns `Vector3f`

  > Adds together two vectors
  
  > 
  ```lua
  local a = Vector3f.new(1, 0.5, 1)
  local b = Vector3f.new(2, -1, -2)
  
  -- (3, -0.5, -1)
  local result = a + b
  ```

### `vector3f:__sub()`
  > Returns `Vector3f`

  > Subtracts two vectors

  > 
  ```lua
  local a = Vector3f.new(6, -2.3, -4)
  local b = Vector3f.new(-3, -2, 2)
  
  -- (9, -0.3, -6)
  local result = a - b
  ```

### `vector3f:__mul()`
  > Returns `Vector3f`

  > Multiplies two vectors
  
  > 
  ```lua
  local a = Vector3f.new(1, 2, 3)
  local b = Vector3f.new(4, 5, 6)
  
  -- (4, 10, 18)
  local result = a * b
  ```

### `vector3f:__div()`
  > Returns `Vector3f`

  > Divides two vectors

  > 
  ```lua
  local a = Vector3f.new(6, 4, 10)
  local b = Vector3f.new(3, 2, 2)
  
  -- (2, 2, 5)
  local result = a / b
  ```
