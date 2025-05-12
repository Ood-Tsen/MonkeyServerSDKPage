//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)

# MonkeyServiceViewModel

[androidJvm]\
open class [MonkeyServiceViewModel](index.md) : [AndroidViewModel](https://developer.android.com/reference/kotlin/androidx/lifecycle/AndroidViewModel.html)

MonkeyServiceViewModel designed to keep a device property and api interface without UI code. There are two major intents for MonkeyServiceViewModel. 

1. get the MonkeyServiceViewModel 

2. trigger a function to MonkeyServiceViewModel 

3. observer LiveData from MonkeyServiceViewModel 

 #java,#Android, 

**How to get a MonkeyServiceViewModel:**

```kotlin

   // get a MonkeyServiceViewModel from getInstance
   MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());

```

**How to trigger a function:**

```kotlin

   // just call the function immedially (e.g. getLanguage)
   // the crosponding result will update in LiveData
   model.getLanguage()

```

**How to observer LiveData:**

```kotlin

   // observeForever the property, it the property is changed by and events or user actions.
   // it will observe and application can do the following action.
   model.language().observeForever(language->{
       Log.i(TAG,"observeForever language " + language);
   });

```

**How to trigger a 'take a photo' on devices**

```kotlin

   // 'take a photo' is a complexed actions. we will show how to do on device.
   // it contains two functions.
   // 1. enableFunctions
   // 2. sendExternalAction with TAKE_PHOTO_ONLY
   List<Pair<FunctionsCommand,Boolean>> options = new ArrayList<>();
   options.add(new Pair(FunctionsCommand.capturePhoto,true));
   model.enableFunctions(options);
   model.sendExternalAction(ExternalAction.TAKE_PHOTO_ONLY);

```

**when do we know the photo is ready after triggering a 'take a photo' on devices**

```kotlin

   // juse observe lastPhotoName
   model.lastPhotoName().observeForever(photoName ->{
   // get ReceivedFile from photoName
       Map<String, ReceivedFile> map = model.receivedFile().getValue();
       ReceivedFile receivedFile = map.get(photoName);

   // get raw data receivedFile
       ByteBuffer buffer = receivedFile.raw;
   }

```

## Functions

| Name | Summary |
|---|---|
| [addProcessMessageResult](add-process-message-result.md) | [androidJvm]<br>open fun [addProcessMessageResult](add-process-message-result.md)(info: [ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md))<br>addProcessMessageResult is a public function. |
| [battery](battery.md) | [androidJvm]<br>open fun [battery](battery.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html)&gt;<br>it present the Device's battery level from 0 to 100. |
| [charging](charging.md) | [androidJvm]<br>open fun [charging](charging.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html)&gt;<br>it present the Device's is charging by USB or not. |
| [enableFunctions](enable-functions.md) | [androidJvm]<br>open fun [enableFunctions](enable-functions.md)(list: [List](https://developer.android.com/reference/kotlin/java/util/List.html)&lt;[Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html)&lt;[FunctionsCommand](../../com.mm.monkey.server.services.enums/-functions-command/index.md), [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html)&gt;&gt;)<br>open fun [enableFunctions](enable-functions.md)(functionsCommand: [FunctionsCommand](../../com.mm.monkey.server.services.enums/-functions-command/index.md), enable: [Boolean](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-boolean/index.html))<br>to enable or disable a single following Device's function. |
| [getInstance](get-instance.md) | [androidJvm]<br>open fun [getInstance](get-instance.md)(@[NonNull](https://developer.android.com/reference/kotlin/androidx/annotation/NonNull.html)application: [Application](https://developer.android.com/reference/kotlin/android/app/Application.html)): [MonkeyServiceViewModel](index.md) |
| [language](language.md) | [androidJvm]<br>open fun [language](language.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html)&gt;<br>it present the Device's voice trigger language. |
| [lastPhotoName](last-photo-name.md) | [androidJvm]<br>open fun [lastPhotoName](last-photo-name.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[String](https://developer.android.com/reference/kotlin/java/lang/String.html)&gt;<br>it keep the lastest photo name called by art_recognition or get_photo_p2p. |
| [lastProcessMessage](last-process-message.md) | [androidJvm]<br>open fun [lastProcessMessage](last-process-message.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md)&gt;<br>is show the last ASK AI message added in processMessageList. |
| [lastThumbnailName](last-thumbnail-name.md) | [androidJvm]<br>open fun [lastThumbnailName](last-thumbnail-name.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[String](https://developer.android.com/reference/kotlin/java/lang/String.html)&gt;<br>it keep the latest thumbnail name called by get_thumbnail. |
| [monkeyConnected](monkey-connected.md) | [androidJvm]<br>open fun [monkeyConnected](monkey-connected.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html)&gt;<br>it presend CA and 3rd app is binded or not. |
| [photoList](photo-list.md) | [androidJvm]<br>open fun [photoList](photo-list.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Map](https://developer.android.com/reference/kotlin/java/util/Map.html)&lt;[String](https://developer.android.com/reference/kotlin/java/lang/String.html), [PhotoItem](../../com.mm.monkey.server.services.data/-photo-item/index.md)&gt;&gt;<br>it may update by calling getPhotoList it keep all photo name and PhotoItem object in a map. |
| [putOn](put-on.md) | [androidJvm]<br>open fun [putOn](put-on.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html)&gt;<br>it presend user put on or take off the Device(Glasses). |
| [queryPhotoList](query-photo-list.md) | [androidJvm]<br>open fun [queryPhotoList](query-photo-list.md)(timestamp: [Long](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-long/index.html))<br>It will create a json commnad to Binder to trigger retrive the all photos' name in Device. |
| [queryPhotoP2P](query-photo-p2-p.md) | [androidJvm]<br>open fun [queryPhotoP2P](query-photo-p2-p.md)(photoName: [String](https://developer.android.com/reference/kotlin/java/lang/String.html))<br>It will create a json commnad to Binder to get the raw of photo from Device. |
| [queryThumbnail](query-thumbnail.md) | [androidJvm]<br>open fun [queryThumbnail](query-thumbnail.md)(photoName: [String](https://developer.android.com/reference/kotlin/java/lang/String.html))<br>It will create a json commnad to Binder to get the Thumbnail of photo from Device. |
| [receivedFile](received-file.md) | [androidJvm]<br>open fun [receivedFile](received-file.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Map](https://developer.android.com/reference/kotlin/java/util/Map.html)&lt;[String](https://developer.android.com/reference/kotlin/java/lang/String.html), [ReceivedFile](../../com.mm.monkey.server.services.data/-received-file/index.md)&gt;&gt;<br>it keep all file name and ReceivedFile object in a map. |
| [removeProcessMessage](remove-process-message.md) | [androidJvm]<br>open fun [removeProcessMessage](remove-process-message.md)(): [ProcessMessageInfo](../../com.mm.monkey.server.services.data/-process-message-info/index.md)<br>getProcessMessage is a public function. |
| [sendExternalAction](send-external-action.md) | [androidJvm]<br>open fun [sendExternalAction](send-external-action.md)(action: [ExternalAction](../../com.mm.monkey.server.services.enums/-external-action/index.md))<br>it will trigger two kind of Action. |
| [storageTotal](storage-total.md) | [androidJvm]<br>open fun [storageTotal](storage-total.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Double](https://developer.android.com/reference/kotlin/java/lang/Double.html)&gt;<br>it present the Device's total storage in GB. |
| [storageUsed](storage-used.md) | [androidJvm]<br>open fun [storageUsed](storage-used.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Double](https://developer.android.com/reference/kotlin/java/lang/Double.html)&gt;<br>it present the Device's used storage in GB. |