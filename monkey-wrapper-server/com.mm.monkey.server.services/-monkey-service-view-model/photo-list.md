//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[photoList](photo-list.md)

# photoList

[androidJvm]\
open fun [photoList](photo-list.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Map](https://developer.android.com/reference/kotlin/java/util/Map.html)&lt;[String](https://developer.android.com/reference/kotlin/java/lang/String.html), [PhotoItem](../../com.mm.monkey.server.services.data/-photo-item/index.md)&gt;&gt;

it may update by calling getPhotoList it keep all photo name and PhotoItem object in a map.

#### Return

- return in Map. 

**How to Trigger:**

```kotlin

final String text = "2011-10-02 18:48:05.123";
ts = Timestamp.valueOf(text);
MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.getPhotoList(ts.getTime());

```
model - the instance of MonkeyServiceViewModel 

**How to Get:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
Map<String,PhotoItem> photomap = model.photoList().getValue();
Collection<PhotoItem> values = photomap.values();
Map<String, ReceivedFile> filemap = model.receivedFile().getValue();
for (PhotoItem item : values) {
  String name = item.getName();
  ReceivedFile file = filemap[name];
}

```
model - the instance of MonkeyServiceViewModel