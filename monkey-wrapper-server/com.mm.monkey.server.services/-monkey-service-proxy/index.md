//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceProxy](index.md)

# MonkeyServiceProxy

[androidJvm]\
abstract class [MonkeyServiceProxy](index.md) : IMonkey.Stub

The main purpose implement the IBinder for com.mm.monkey.sdk.IMonkey #java,#Android, 

**How to Use:**

Create a class extends from MonkeyServiceProxy 

```kotlin

   public class MonkeyServiceImpl extends MonkeyServiceProxy{

   }

```

Create a service extends from com.mm.monkey.server.services.LifeBaseService 

It uses LifeBaseService to handle the lifecycle for livedata

```kotlin

public class MonkeyService extends com.mm.monkey.server.services.LifeBaseService{
  
  public void onCreate() {
  TAG = "MonkeyService";
  if (mBinder == null)
    mBinder = (IBinder) new MonkeyServiceImpl(this);
    super.onCreate();
  }
}

```

## Functions

| Name | Summary |
|---|---|
| [fromEvent](from-event.md) | [androidJvm]<br>fun [fromEvent](from-event.md)(className: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), event: [String](https://developer.android.com/reference/kotlin/java/lang/String.html))<br>fromEvent is a final function. |
| [getDescription](get-description.md) | [androidJvm]<br>open fun [getDescription](get-description.md)(locale: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>getDescription check permission defined in the Annotation 'Permission' of the function MonkeyClient. |
| [onReceiveFile](on-receive-file.md) | [androidJvm]<br>fun [onReceiveFile](on-receive-file.md)(s: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>onReceiveFile is a internal final function. |
| [processMessage](process-message.md) | [androidJvm]<br>fun [processMessage](process-message.md)(json: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>processMessage is used by SDK. |
| [processMessageAndImage](process-message-and-image.md) | [androidJvm]<br>fun [processMessageAndImage](process-message-and-image.md)(json: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), payload: MyPayload): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>processMessageAndImage is used by SDK, |
| [processMessageAndImageEx](process-message-and-image-ex.md) | [androidJvm]<br>abstract fun [processMessageAndImageEx](process-message-and-image-ex.md)(info: [ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md), payload: MyPayload): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>processMessageAndImageEx process info and payload from binder of the function MonkeyClient. |
| [processMessageEx](process-message-ex.md) | [androidJvm]<br>abstract fun [processMessageEx](process-message-ex.md)(info: [ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md)): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)<br>processMessage check permission defined in the Annotation 'Permission' of the function MonkeyClient. |
| [setNotificationListener](set-notification-listener.md) | [androidJvm]<br>fun [setNotificationListener](set-notification-listener.md)(listener: INotificationListener)<br>The function setNotificationListener will notify message from service to caller. |