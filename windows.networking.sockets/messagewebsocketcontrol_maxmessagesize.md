---
-api-id: P:Windows.Networking.Sockets.MessageWebSocketControl.MaxMessageSize
-api-type: winrt property
---

<!-- Property syntax
public uint MaxMessageSize { get;  set; }
-->

# Windows.Networking.Sockets.MessageWebSocketControl.MaxMessageSize

## -description
The maximum message size, in bytes, for a WebSocket message to be configured on the [MessageWebSocket](messagewebsocket.md) object.

## -property-value
The maximum message size, in bytes, to be configured on the [MessageWebSocket](messagewebsocket.md) object.

## -remarks
The [MaxMessageSize](messagewebsocketcontrol_maxmessagesize.md) property is used to configure the maximum size of a WebSocket message on a [MessageWebSocket](messagewebsocket.md) object. If a message exceeds this size, [MessageReceived](messagewebsocket_messagereceived.md) event will be raised on the [MessageWebSocket](messagewebsocket.md) object, and the [GetDataReader](messagewebsocketmessagereceivedeventargs_getdatareader.md) or [GetDataStream](messagewebsocketmessagereceivedeventargs_getdatastream.md) method on the [MessageWebSocketMessageReceivedEventArgs](messagewebsocketmessagereceivedeventargs.md) callback parameter will fail (with an error code indicating that the maximum message size has been exceeded).

The default value for the [MaxMessageSize](messagewebsocketcontrol_maxmessagesize.md) property is INFINITE.

The [MaxMessageSize](messagewebsocketcontrol_maxmessagesize.md) property can only be set before calling the [ConnectAsync](messagewebsocket_connectasync.md) method on the [MessageWebSocket](messagewebsocket.md) object. If the [MessageWebSocket](messagewebsocket.md) is already connected, an attempt to set this property will return an error.

## -examples

## -see-also
[How to use advanced WebSocket controls ](http://msdn.microsoft.com/library/0a47f7c3-66f9-4315-886e-bd1afe77bf39), [How to use advanced WebSocket controls ](http://msdn.microsoft.com/library/4ab9621e-90e5-420e-88d0-09f1c7239d7a), [MessageWebSocket](messagewebsocket.md)