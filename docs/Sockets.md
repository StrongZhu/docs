Sockets
=

Sockets are used to determine which inputs and outputs can be connected. This can indicate the type of data that can be transferred from one node to another.

First of all you should declare all sockets that will be used in the editor

```js
var numSocket = new Rete.Socket('Number value');
var strSocket = new Rete.Socket('String');
```

The parameter **name** must be unique. With the same class name, styles must be defined to make the sockets visually different (not only background)

```css
.socket.number-value {
    background: #96b38a
}
```

As a result you can connect only the inputs and outputs with the same sockets. Although there may be situations when you need to connect different sockets. To do this, there is a method **combineWith**:

```js
var anyTypeSocket = new Rete.Socket('Any type');
numSocket.combineWith(anyTypeSocket);
```
Now you can connect *numSocket* to *anyTypeSocket*, but not vice versa