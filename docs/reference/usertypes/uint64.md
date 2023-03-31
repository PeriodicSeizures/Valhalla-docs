# UInt64

Wrapper type for 64-bit unsigned integers because of Luas inability to support them

### `UInt64.new(...)`
  > Returns `UUInt64`
  
  > `UInt64.new()`, `UInt64.new(number)`, `UInt64.new(lower, upper)`,
    `UInt64.new(hexstring)`
  
### `uint64:tonumber()`
  > Returns `number`
  
  > Directly returns the underlying value as a Lua number
  
  > This should only be called assuming the integral value 
    can be represented by a double (up to numbers ~2^35)

## Metamethods / operators
    
### `uint64:__add()`
  > Returns `UInt64`
  
### `uint64:__sub()`
  > Returns `UInt64`
  
### `uint64:__mul()`
  > Returns `UInt64`
  
### `uint64:__div()`
  > Returns `UInt64`
  
### `uint64:__divi()`
  > Returns `UInt64`
  
### `uint64:__unm()`
  > Returns `UInt64`
  
  > Unary minus
  
  > `-uint64`
  
### `uint64:__eq()`
  > Returns `UInt64`
  
### `uint64:__lt()`
  > Returns `UInt64`
  
### `uint64:__leq()`
  > Returns `UInt64`
  