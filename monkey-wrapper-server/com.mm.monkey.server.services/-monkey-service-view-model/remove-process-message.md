//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[removeProcessMessage](remove-process-message.md)

# removeProcessMessage

[androidJvm]\
open fun [removeProcessMessage](remove-process-message.md)(): [ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md)

getProcessMessage is a public function. the calling follow is 

1. sendExternalAction by 3rd APP to CA.

2. addProcessMessage from CA to 3rd App.

3. getProcessMessage by 3rd APP.

4. addProcessMessageResult by 3rd.

5. getProcessMessageResult by CA.

#### Return

- return in ProcessMessageInfo, including the request, and method, 

**How to Trigger:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.sendExternalAction(ExternalAction.TAKE_PHOTO_AND_TEXT_MESSAGE);

```
model - the instance of MonkeyServiceViewModel. 

**How to GET Text from Voice:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
ProcessMessageInfo info = model.getProcessMessage()
TextView text = findViewById(R.id.procrss_message_value);
text.setText(info.text);

```
model - the instance of MonkeyServiceViewModel.