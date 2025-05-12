//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[addProcessMessageResult](add-process-message-result.md)

# addProcessMessageResult

[androidJvm]\
open fun [addProcessMessageResult](add-process-message-result.md)(info: [ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md))

addProcessMessageResult is a public function. the calling follow is 

1. sendExternalAction by 3rd APP to CA.

2. addProcessMessage from CA to 3rd App.

3. getProcessMessage by 3rd APP

4. addProcessMessageResult by 3rd App.

5. getProcessMessageResult by CA.

#### Return

- void 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.lastProcessMessage().observeForever(info ->{
  //procresss message and get a answer
  String result = MonkeyCommandResult.success("This is a paint.", "EN-US");
  info.result = result;
  model.addProcessMessageResult(info);
}

```
model - the instance of MonkeyServiceViewModel 

use model.lastProcessMessage() to observer the last ProcessMessage. 

In ProcessMessage , we can get user asked message. 

And update our answer back info.result = result 

Finally, return this ProcessMessage with answer by calling model.addProcessMessageResult.

#### Parameters

androidJvm

| | |
|---|---|
| info | - pass ProcessMessageInfo |