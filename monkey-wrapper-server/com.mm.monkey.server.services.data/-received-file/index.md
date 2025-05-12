//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services.data](../index.md)/[ReceivedFile](index.md)

# ReceivedFile

[androidJvm]\
open class [ReceivedFile](index.md)

ReceivedFile handle received ByteBuffer from binder. it keeps in the model.receivedFile(); 

How to Use:

```kotlin
model = MonkeyServiceViewModel.getInstance(getApplication());
Mapmap = model.receivedFile().getValue();
ReceivedFile receivedFile = map.get(fileName);
ByteBuffer bytebuffer = receivedFile.raw;
model - MonkeyServiceViewModel.
receivedFile - ReceivedFile
bytebuffer - receivedFile.raw
```

## Constructors

| | |
|---|---|
| [ReceivedFile](-received-file.md) | [androidJvm]<br>constructor(action: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), fileName: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), raw: [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html)) |

## Properties

| Name | Summary |
|---|---|
| [action](action.md) | [androidJvm]<br>val [action](action.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html) |
| [fileName](file-name.md) | [androidJvm]<br>val [fileName](file-name.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html) |
| [raw](raw.md) | [androidJvm]<br>val [raw](raw.md): [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html) |