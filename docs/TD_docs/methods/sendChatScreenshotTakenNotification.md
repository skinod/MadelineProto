---
title: sendChatScreenshotTakenNotification
description: Sends notification about screenshot taken in a chat. Works only in secret chats
---
## Method: sendChatScreenshotTakenNotification  
[Back to methods index](index.md)


Sends notification about screenshot taken in a chat. Works only in secret chats

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|chat\_id|[long](../types/long.md) | Yes|Chat identifier|


### Return type: [Ok](../types/Ok.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) {
    $this->bot_login($token);
}
if (isset($number)) {
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$Ok = $MadelineProto->sendChatScreenshotTakenNotification(['chat_id' => long, ]);
```

Or, if you're into Lua:

```
Ok = sendChatScreenshotTakenNotification({chat_id=long, })
```

