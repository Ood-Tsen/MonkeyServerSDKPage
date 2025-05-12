//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceProxy](index.md)/[processMessageEx](process-message-ex.md)

# processMessageEx

[androidJvm]\
abstract fun [processMessageEx](process-message-ex.md)(info: [ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md)): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)

processMessage check permission defined in the Annotation 'Permission' of the function MonkeyClient.processMessage

#### Return

RESULT_SUCCESS ,RESULT_FAILED, RESULT_PROCESSING 

**How to Use:**

```kotlin

// after extend from MonkeyServiceProxy
public String processMessageEx(ProcessMessageInfo info) throws RemoteException {
   // get the requestMessage
   String requestMessage = info.getRequest().text;
   // check the request language.
   Locale locale = LocaleUtils.fromString(cmd.locale);
   // make an answer.
   String answerText = "This is a paint";
   // set answer to ProcessMessageInfo
   info.setResultSuccess(answerText, locale);
   // send back to Binder
   answerFromAi(info);

   return RESULT_SUCCESS;
}

```

#### Parameters

androidJvm

| |
|---|
| info |