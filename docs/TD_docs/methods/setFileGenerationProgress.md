---
title: setFileGenerationProgress
description: Next part of a file was generated
---
## Method: setFileGenerationProgress  
[Back to methods index](index.md)


Next part of a file was generated

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|generation\_id|[long](../types/long.md) | Yes|Identifier of the generation process|
|ready|[int](../types/int.md) | Yes|Number of bytes already generated. Negative number means that generation has failed and should be terminated|


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

$Ok = $MadelineProto->setFileGenerationProgress(['generation_id' => long, 'ready' => int, ]);
```

Or, if you're into Lua:

```
Ok = setFileGenerationProgress({generation_id=long, ready=int, })
```

