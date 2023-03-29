# Vector2i

*I like this quote format more than Vector3...*

### `Vector2i.new()`
  > Returns `Vector2i`

  > Constructs a Vector2i equal to Vector2i.ZERO

### `Vector2i.new(x, y, z)`
  > Returns `Vector2i`

  > Constructs a Vector2i from x, y, and z parameters

### `Vector2i.__add(other)`
  > Returns `Vector2i`

  > Adds together this and another vector, returning a new vector

### `Vector2i.__sub(other)`
  > Returns `Vector2i`

  > Subtracts a vector from this, returning a new vector

### `Vector2i.x`
  > Returns `number`

  > The x component of the vector

### `Vector2i.y`
  > Returns `number`

  > The y component of the vector

### `Vector2i:Distance(other)`
  > Returns `number`

  > The distance between this and another vector

### `Vector2i.magnitude`
  > Result: `number` | readonly

The magnitude of the vector

### `Vector2i:Normalize()`
  > Result: `Vector2i&`
  
  > *Note: using an temporary reference might break things*

  > Normalizes the vector and return this

### `Vector2i.normalized`
  > Result: `Vector2i` | readonly

  > Returns a new normalized this

### `Vector2i.SqDistance(other)`
  > Result: `number`

  > Returns the squared distance between this and another vector
