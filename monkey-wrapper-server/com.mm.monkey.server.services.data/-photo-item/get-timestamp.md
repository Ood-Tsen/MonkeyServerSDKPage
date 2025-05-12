//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services.data](../index.md)/[PhotoItem](index.md)/[getTimestamp](get-timestamp.md)

# getTimestamp

[androidJvm]\
open fun [getTimestamp](get-timestamp.md)(): [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp.html)

Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT 

How to Use:

```kotlin
model = MonkeyServiceViewModel.getInstance(getApplication());
Mapmap = model.photoList().getValue();
PhotoItem item = map.get(fileName);
Timestamp ts = item.getTimeStamp();
```

#### Return