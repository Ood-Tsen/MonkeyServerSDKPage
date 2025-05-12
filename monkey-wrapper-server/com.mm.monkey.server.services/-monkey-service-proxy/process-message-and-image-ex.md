//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceProxy](index.md)/[processMessageAndImageEx](process-message-and-image-ex.md)

# processMessageAndImageEx

[androidJvm]\
abstract fun [processMessageAndImageEx](process-message-and-image-ex.md)(info: [ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md), payload: MyPayload): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)

processMessageAndImageEx process info and payload from binder of the function MonkeyClient.processMessageAndImage

#### Return

RESULT_SUCCESS 

**How to Use:**

```kotlin

// after extend from MonkeyServiceProxy
public String processMessageAndImageEx(ProcessMessageInfo info, MyPayload payload) throws RemoteException {
   // get the request
   String requestMessage = info.getRequest().text;
   // check the request language.
   Locale locale = LocaleUtils.fromString(info.getRequest().locale);
   // get image from payload.
   byte[] bytearray = payload.byteArray;
   // make an answer.
   String answerText = "This is a paint";
   // set answer to ProcessMessageInfo
   info.setResultSuccess(answerText, locale);
   // send back to CA
   answerFromAi(info);

   return RESULT_SUCCESS;
}

```

#### Parameters

androidJvm

| |
|---|
| info |
| payload |