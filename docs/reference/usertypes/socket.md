# Socket

The socket structure used throughout the game for Rpc-pings and Rpc invocations
    
### `socket.connected`
  > Returns `boolean` | **readonly**
  
  > Whether the socket is connected or disconnected
  
### `socket.address`
  > Returns `string` | **readonly**
  
  > The address of the remote socket
  
### `socket.host`
  > Returns `string` | **readonly**
  
  > The hostname of the remote socket
  
  > This value will always be unique for any given connection, 
  and can be safely used to differentiate connections.
  
### `socket.sendQueueSize`
  > Returns `number` | **readonly**
  
  > The total size of outgoing data in bytes. 
  
### `socket:Close(flush)`
  > Closes the socket immediately or lingers for a short time
  
  > If flush is true:
    incoming data is discarded
    outgoing data is sent for the next `1` to `3` seconds