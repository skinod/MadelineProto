---
title: inputBotInlineMessageMediaContact
description: inputBotInlineMessageMediaContact attributes, type and example
---
## Constructor: inputBotInlineMessageMediaContact  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|phone\_number|[string](../types/string.md) | Yes|
|first\_name|[string](../types/string.md) | Yes|
|last\_name|[string](../types/string.md) | Yes|
|reply\_markup|[ReplyMarkup](../types/ReplyMarkup.md) | Optional|



### Type: [InputBotInlineMessage](../types/InputBotInlineMessage.md)


### Example:

```
$inputBotInlineMessageMediaContact = ['_' => 'inputBotInlineMessageMediaContact', 'phone_number' => string, 'first_name' => string, 'last_name' => string, 'reply_markup' => ReplyMarkup, ];
```  

Or, if you're into Lua:  


```
inputBotInlineMessageMediaContact={_='inputBotInlineMessageMediaContact', phone_number=string, first_name=string, last_name=string, reply_markup=ReplyMarkup, }

```


