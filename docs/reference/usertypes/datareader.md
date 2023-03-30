# DataReader

A fast utility class for deserializing objects

Note: Any of the Read...() methods below will throw if the length is exceeded. 
Objects which start with a 32-bit signed size will throw if the size is negative.

### `DataReader.new(bytes)`
  > Returns `DataReader`

  > Constructs a DataReader using a specified byte buffer

  > This object must not exist beyond the scope of its
  underlying vector. Doing so will cause segfaults.
  
### `dataReader.provider`
  > Returns `Bytes`
  
  > The underlying byte buffer of the reader
  
### `dataReader.pos`
  > Returns `number`
  
  > The current position of the reader
  
  > Will throw if set position is invalid (negative or outside bounds)
  
### `dataReader:ReadBool()`
  > Returns `boolean`
  
  > Reads a boolean from the stream and advances the position by `1`
  
### `dataReader:ReadString()`
  > Returns `string`
  
  > Reads a string from the stream and advances the position by `4 + <size>`

### `dataReader:ReadStrings()`
  > Returns `strings`
  
  > Reads several strings from the stream and advances the position by `4 + <count>`
  
### `dataReader:ReadBytes()`
  > Returns `Bytes`
  
  > Reads a byte buffer from the stream and advances the position by `4 + <size>`
  
### `dataReader:ReadZDOID()`
  > Returns `ZDOID`
  
  > Reads a ZDOID from the stream and advances the position by `12`
  
### `dataReader:ReadVector3()`
  > Returns `Vector3`
  
  > Reads a Vector3 from the stream and advances the position by `12`
  
### `dataReader:ReadVector2i()`
  > Returns `Vector2i`
  
  > Reads a Vector2i from the stream and advances the position by `8`
  
### `dataReader:ReadQuaternion()`
  > Returns `Quaternion`
  
  > Reads a Quaternion from the stream and advances the position by `16`
  
### `dataReader:ReadProfile()`
  > Returns `UserProfile`
  
  > Reads a UserProfile from the stream and advances the position by `16`
  
### `dataReader:ReadInt8()`
  > Returns `number`
  
  > Reads an 8-bit signed integer from the stream and advances the position by `1`
  
### `dataReader:ReadInt16()`
  > Returns `number`
  
  > Reads a 16-bit signed integer from the stream and advances the position by `2`
  
### `dataReader:ReadInt32()`
  > Returns `number`
  
  > Reads a 32-bit signed integer from the stream and advances the position by `4`
  
### `dataReader:ReadInt64()`
  > Returns `Int64`
  
  > Reads a 64-bit signed integer from the stream and advances the position by `8`
  
### `dataReader:ReadUInt8()`
  > Returns `number`
  
  > Reads an 8-bit unsigned integer from the stream and advances the position by `1`
  
### `dataReader:ReadUInt16()`
  > Returns `number`
  
  > Reads an 16-bit unsigned integer from the stream and advances the position by `2`
  
### `dataReader:ReadUInt32()`
  > Returns `number`
  
  > Reads an 32-bit unsigned integer from the stream and advances the position by `4`
  
### `dataReader:ReadUInt64()`
  > Returns `UInt64`
  
  > Reads an 64-bit unsigned integer from the stream and advances the position by `8`
  
### `dataReader:ReadFloat()`
  > Returns `number`
  
  > Reads a 32-bit floating point number from the stream and advances the position by `4`
  
### `dataReader:ReadDouble()`
  > Returns `number`
  
  > Reads a 64-bit floating point number from the stream and advances the position by `8`
  
### `dataReader:ReadChar()`
  > Returns `number`
  
  > Reads a variable length UTF8 character from the stream and advances the position by a max of `3`
  