//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[lastThumbnailName](last-thumbnail-name.md)

# lastThumbnailName

[androidJvm]\
open fun [lastThumbnailName](last-thumbnail-name.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[String](https://developer.android.com/reference/kotlin/java/lang/String.html)&gt;

it keep the latest thumbnail name called by get_thumbnail.

#### Return

- return in String. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
String fileName = model.lastThumbnailName().getValue();
Map<String, ReceivedFile> fileMap = model.receivedFile().getValue();
//get ReceivedFile from filename
ReceivedFile file = fileMap[fileName];

```
model - the instance of MonkeyServiceViewModel. 

call model.lastThumbnailName().getValue() to get last received thumbnail file name. 

call model.receivedFile().getValue() to get fileMap object, 

and use fileName to get the ReceivedFile object.