# Bytes

A byte buffer used in io operations. 

Buffer operations are managed by sol container wrappers. 
This means that this object is essentially a 
`std::vector<uint8_t>`. See [sol containers](https://sol2.readthedocs.io/en/latest/containers.html#container-operations)
for more information.

### `Bytes.new()`
  > Returns `Bytes`
  
  > Creates an empty byte buffer

### `Bytes.new(other)`
  > Returns `Bytes`
  
  > Creates an bytes buffer with contents copied from another buffer
  
### `bytes:Assign(other)`
  > Assigns the contents from another buffer to this

### `bytes:Move(other)`
  > Efficiently moves the contents from another buffer to this

### `bytes:Swap(other)`
  > Efficiently swaps the contents between another buffer and this