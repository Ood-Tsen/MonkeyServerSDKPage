//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[lastProcessMessage](last-process-message.md)

# lastProcessMessage

[androidJvm]\
open fun [lastProcessMessage](last-process-message.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md)&gt;

is show the last ASK AI message added in processMessageList.

#### Return

- return in ProcessMessageInfo. 

**How to Trigger:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.sendExternalAction(ExternalAction.TAKE_PHOTO_AND_TEXT_MESSAGE);

```
model - the instance of MonkeyServiceViewModel. 

**How to GET Text from Voice:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.lastProcessMessage().observeForever(info ->{
TextView text = findViewById(R.id.procrss_message_value);
text.setText(info.text);
}

```
model - the instance of MonkeyServiceViewModel.