//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[queryPhotoList](query-photo-list.md)

# queryPhotoList

[androidJvm]\
open fun [queryPhotoList](query-photo-list.md)(timestamp: [Long](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-long/index.html))

It will create a json commnad to Binder to trigger retrive the all photos' name in Device.

#### Return

- void 

**How to Get:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
final String datetimestring = "2011-10-02 18:48:05.123";
ts = Timestamp.valueOf(datetimestring);
model.queryPhotoList(ts.getTime());

```
model - the instance of MonkeyServiceViewModel. 

crate a ts from Timestamp.valueOf(datetimestring) 

call model.queryPhotoList with ts

**How to Get:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
Map<String,PhotoItem> photomap = model.photoList().getValue();
Collection<PhotoItem> values = photomap.values();
Map<String, ReceivedFile> filemap = model.receivedFile().getValue();
for (PhotoItem item : values) {
  String filename = item.getName();
  ReceivedFile file = filemap[filename];
}

```
model - the instance of MonkeyServiceViewModel. 

calling model.photoList().getValue() to get Map object which containing saved photos taken after the timestamp. 

use filename to get the ReceivedFile.

#### Parameters

androidJvm

| | |
|---|---|
| timestamp | - filter the picture taken after the timestamp. |