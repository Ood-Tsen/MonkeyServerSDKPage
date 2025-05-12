//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[sendExternalAction](send-external-action.md)

# sendExternalAction

[androidJvm]\
open fun [sendExternalAction](send-external-action.md)(action: [ExternalAction](../../com.mm.monkey.server.services.enums/-external-action/index.md))

it will trigger two kind of Action. 1. take a photo and use this photo to ask AI. 2. take a photo and a message from voice and use these to ask AI.

#### Return

- void 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.sendExternalAction(ExternalAction.TAKE_PHOTO_AND_TEXT_MESSAGE);

```
model - the instance of MonkeyServiceViewModel. 

call model.sendExternalAction to take a photo or take a photo with text message.

#### Parameters

androidJvm

| | |
|---|---|
| action | - in ExternalAction |