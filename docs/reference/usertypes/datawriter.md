# DataWriter

A fast utility class for serializing objects

### `DataWriter.new(bytes)`
  > Returns `DataWriter`

  > Constructs a DataWriter using a specified buffer

  > This object must not exist beyond the scope of its
  underlying vector. Doing so will cause segfaults.
  
### `dataWriter.provider`
  > Returns `bytes`
  
  > The underlying buffer of the writer
  
### `dataWriter.pos`
  > Returns `number`
  
  > The current position of the writer
  
### `dataWriter:Clear()`
  > Clears the underlying buffer and sets `pos` to 0
  
### `dataWriter:Write(object)`
  > An overload for writing an object to the underlying buffer
  
  > Overloads: `boolean`, `string`, `list<string>`, `bytes`, `ZDOID`, `Vector3`, 
  ` Vector2i`, `Quaternion`, `UserProfile`
  
### `dataWriter:WriteInt8(value)`
  > Writes a `number` as a signed 8 bit integer
  
### `dataWriter:WriteInt16(value)`
  > Writes a `number` as a signed 16 bit integer
  
### `dataWriter:WriteInt32(value)`
  > Writes a `number` as a signed 32 bit integer
  
### `dataWriter:WriteInt64(value: Int64)`
  > Writes a `Int64` as a signed 64 bit integer
  
### `dataWriter:WriteUInt8(value)`
  > Writes a `number` as an unsigned 8 bit integer
  
### `dataWriter:WriteUInt16(value)`
  > Writes a `number` as an unsigned 16 bit integer
  
### `dataWriter:WriteUInt32(value)`
  > Writes a `number` as an unsigned 32 bit integer
  
### `dataWriter:WriteUInt64(value: UInt64)`
  > Writes a `UInt64` as an unsigned 64 bit integer
  
### `dataWriter:WriteFloat(value)`
  > Writes a `number` as an 32 bit floating point number
  
### `dataWriter:WriteDouble(value)`
  > Writes a `number` as an 64 bit floating point number
  
### `dataWriter:WriteChar(value)`
  > Writes a `number` as a variable length UTF8 character
  
  > Must fit within a c++ `char16_t`
  
  > Up to `3` bytes will be written