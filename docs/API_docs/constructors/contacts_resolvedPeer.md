## Constructor: contacts\_resolvedPeer  

### Attributes:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|peer|[Peer](../types/Peer.md) | Required|
|chats|Array of [Chat](../types/Chat.md) | Required|
|users|Array of [User](../types/User.md) | Required|


### Type: [contacts\_ResolvedPeer](../types/contacts\_ResolvedPeer.md)

### Example:


```
$contacts_resolvedPeer = ['peer' => Peer, 'chats' => [Chat], 'users' => [User], ];
```