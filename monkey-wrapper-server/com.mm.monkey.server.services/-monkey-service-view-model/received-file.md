//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[receivedFile](received-file.md)

# receivedFile

[androidJvm]\
open fun [receivedFile](received-file.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Map](https://developer.android.com/reference/kotlin/java/util/Map.html)&lt;[String](https://developer.android.com/reference/kotlin/java/lang/String.html), [ReceivedFile](../../com.mm.monkey.server.services.data/-received-file/index.md)&gt;&gt;

it keep all file name and ReceivedFile object in a map.

#### Return

- return in Map. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
Map<String, ReceivedFile> fileMap = model.receivedFile().getValue();
//get ReceivedFile from filename
ReceivedFile file = fileMap[filename];
//get encoded raw data from receivedFile
ByteBuffer hevcByteBuffer = receivedFile.raw;
//pass ByteBuffer to inputstream
InputStream inputStream = byteBufferToInputStream(hevcByteBuffer);
//pass inputstream to bitmap to decode
Bitmap bitmap = BitmapFactory.decodeStream(inputStream);

```
model - the instance of MonkeyServiceViewModel 

call model.receivedFile().getValue() to get fileMap object. In fileMap, and use fileName to get the ReceivedFile object. 

call receivedFile.raw to get compressed binary raw data for fileName, its format is ByteBuffer. 

In this case, the binary raw data is a picture, use BitmapFactory to decode this compressed raw data into Bitmap object.