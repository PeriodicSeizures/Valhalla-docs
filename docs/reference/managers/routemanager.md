# RouteManager

### `RouteManager:Register(sig, function)`
  > Registers a RoutedRpc function

### `RouteManager:InvokeView(target, zdoid, methodRepr, ...)`
  > Invokes a RoutedRpc aimed towards a peer(s) specified ZNetView object
  
  > Optionally accepts variadic args `...` that are passed to the remote function

### `RouteManager:Invoke(target, methodRepr, ...)`
  > Invokes a RoutedRpc aimed towards a peer(s)

### `RouteManager:InvokeAll(methodRepr, ...)`
  > Invokes a RoutedRpc aimed towards all peers