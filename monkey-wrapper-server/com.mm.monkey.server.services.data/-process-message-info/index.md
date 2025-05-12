//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services.data](../index.md)/[ProcessMessageInfo](index.md)

# ProcessMessageInfo

[androidJvm]\
open class [ProcessMessageInfo](index.md)

ProcessMessageInfo is a data class for processMessageEx and processMessageAndImageEx. field request - the request json from binder. field method - processMessage or processMessageAndImage. field result - the answer json to binder. 

**How to Use:**

```kotlin

// after extend from MonkeyServiceProxy
public String processMessageEx(ProcessMessageInfo info) throws RemoteException {
   // get the request message
   String requestMessage = info.getRequest().text;
   // get the locale of request message.
   Locale locale = LocaleUtils.fromString(info.getRequest().locale);
   info.setResultSuccess("This is a paint.", locale);
}
info - ProcessMessageInfo

```

## Constructors

| | |
|---|---|
| [ProcessMessageInfo](-process-message-info.md) | [androidJvm]<br>constructor(request: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), method: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)) |

## Properties

| Name | Summary |
|---|---|
| [method](method.md) | [androidJvm]<br>val [method](method.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>methiod will be processMessage or processMessageAndImage |
| [request](request.md) | [androidJvm]<br>val [request](request.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>request is from json, the format is json |
| [result](result.md) | [androidJvm]<br>open var [result](result.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>the answer of request, the format is json |

## Functions

| Name | Summary |
|---|---|
| [getRequest](get-request.md) | [androidJvm]<br>open fun [getRequest](get-request.md)(): MonkeyCommandRequest<br>return requst in MonkeyCommandRequest |
| [getResult](get-result.md) | [androidJvm]<br>open fun [getResult](get-result.md)(): MonkeyCommandResult<br>return result in MonkeyCommandResult |
| [setResultFailed](set-result-failed.md) | [androidJvm]<br>open fun [setResultFailed](set-result-failed.md)(answerText: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), locale: [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html))<br>Make result failed |
| [setResultSuccess](set-result-success.md) | [androidJvm]<br>open fun [setResultSuccess](set-result-success.md)(answerText: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), locale: [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html))<br>Make result success |