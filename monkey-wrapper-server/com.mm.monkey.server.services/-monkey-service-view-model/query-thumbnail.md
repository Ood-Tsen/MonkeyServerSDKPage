//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[queryThumbnail](query-thumbnail.md)

# queryThumbnail

[androidJvm]\
open fun [queryThumbnail](query-thumbnail.md)(photoName: [String](https://developer.android.com/reference/kotlin/java/lang/String.html))

It will create a json commnad to Binder to get the Thumbnail of photo from Device. It will use BLE or Wifi to transform the thumbnail

#### Return

- void 

**How to Trigger:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.queryThumbnail(photoName);

```
model - the instance of MonkeyServiceViewModel. 

**How to Get:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
String name = model.lastThumbnailName().getValue();
Collection<PhotoItem> values = photomap.values();
Map<String, ReceivedFile> filemap = model.receivedFile().getValue();
ReceivedFile file = filemap[name];

```
model - the instance of MonkeyServiceViewModel.

#### Parameters

androidJvm

| | |
|---|---|
| photoName | - the photoName is the file name of photo. |