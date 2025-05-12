//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services.data](../index.md)/[PhotoItem](index.md)

# PhotoItem

[androidJvm]\
open class [PhotoItem](index.md)

PhotoItem handle saved pictures on binder. it keeps in the model.photoList() 

How to Use:

```kotlin
model = MonkeyServiceViewModel.getInstance(getApplication());
Mapmap = model.photoList().getValue();
PhotoItem item = map.get(fileName);

model - MonkeyServiceViewModel.
fileName - the fileName of PhotoItem, it is the key to get from photoList();
item - PhotoItem
```

## Constructors

| | |
|---|---|
| [PhotoItem](-photo-item.md) | [androidJvm]<br>constructor(name: [String](https://developer.android.com/reference/kotlin/java/lang/String.html), timestamp: [Long](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-long/index.html)) |

## Properties

| Name | Summary |
|---|---|
| [name](name.md) | [androidJvm]<br>open val [name](name.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html) |

## Functions

| Name | Summary |
|---|---|
| [getTimestamp](get-timestamp.md) | [androidJvm]<br>open fun [getTimestamp](get-timestamp.md)(): [Timestamp](https://developer.android.com/reference/kotlin/java/sql/Timestamp.html)<br>Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT How to Use:```kotlin model = MonkeyServiceViewModel.getInstance(getApplication()); Mapmap = model.photoList().getValue(); PhotoItem item = map.get(fileName); Timestamp ts = item.getTimeStamp(); ``` |