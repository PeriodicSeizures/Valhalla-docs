# Vector3

### `Vector3.new()`
  - Result: `Vector3`

Constructs a Vector3 equal to Vector3.ZERO

### `Vector3.new(x, y, z)`
  - Result: `Vector3`

Constructs a Vector3 from x, y, and z parameters

### `vector3.__add(other)`
  - Result: `Vector3`

Adds together this and another vector, returning a new vector

### `vector3.__sub(other)`
  - Result: `Vector3`

Subtracts a vector from this, returning a new vector

### `vector3.x`
  - Result: `number`
  - Mode: Set or get.

The x component of the vector

### `vector3.y`
  - Result: `number`
  - Mode: Set or get.

The y component of the vector

### `vector3.z`
  - Result: `number`
  - Mode: Set or get.

The z component of the vector

### `vector3:Distance(other)`
  - Result: `number`

The distance between this and another vector

### `vector3.magnitude`
  - Result: `number`
  - Mode: Get only.

The magnitude of the vector

### `vector3:Normalize()`
  - Result: `Vector3&`
  - *Note: using an temporary reference might break things*

Normalizes the vector and return this

### `vector3.normalized`
  - Result: `Vector3`
  - Mode: Get only.

Returns a new normalized this

### `vector3.SqDistance(other)`
  - Result: `number`

Returns the squared distance between this and another vector
