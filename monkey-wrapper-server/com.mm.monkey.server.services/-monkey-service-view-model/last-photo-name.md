//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[lastPhotoName](last-photo-name.md)

# lastPhotoName

[androidJvm]\
open fun [lastPhotoName](last-photo-name.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[String](https://developer.android.com/reference/kotlin/java/lang/String.html)&gt;

it keep the lastest photo name called by art_recognition or get_photo_p2p.

#### Return

- return in String. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
String fileName = model.lastPhotoName().getValue();
Map<String, ReceivedFile> fileMap = model.receivedFile().getValue();
//get ReceivedFile from filename
ReceivedFile file = fileMap[fileName];

```
model - the instance of MonkeyServiceViewModel. 

call model.lastPhotoName().getValue() to get last received thumbnail file name. 

call model.receivedFile().getValue() to get fileMap object, 

and use fileName to get the ReceivedFile object.