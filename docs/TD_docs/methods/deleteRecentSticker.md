---
title: deleteRecentSticker
description: Removes a sticker from the list of recently used stickers
---
## Method: deleteRecentSticker  
[Back to methods index](index.md)


Removes a sticker from the list of recently used stickers

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|is\_attached|[Bool](../types/Bool.md) | Yes|Pass true to remove the sticker from the list of stickers recently attached to photo or video files, pass false to remove the sticker from the list of recently sent stickers|
|sticker|[InputFile](../types/InputFile.md) | Yes|Sticker file to delete|


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

$Ok = $MadelineProto->deleteRecentSticker(['is_attached' => Bool, 'sticker' => InputFile, ]);
```

Or, if you're into Lua:

```
Ok = deleteRecentSticker({is_attached=Bool, sticker=InputFile, })
```

