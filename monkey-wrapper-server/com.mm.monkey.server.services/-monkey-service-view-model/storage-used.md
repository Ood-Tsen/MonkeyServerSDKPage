//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[storageUsed](storage-used.md)

# storageUsed

[androidJvm]\
open fun [storageUsed](storage-used.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Double](https://developer.android.com/reference/kotlin/java/lang/Double.html)&gt;

it present the Device's used storage in GB.

#### Return

- return in Double. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
if(model.storageUsed().getValue() < 3){
    Log.i(TAG," the free storage is less than 3 GB");
}

```
model - the instance of MonkeyServiceViewModel 

call model.storageUsed().getValue() to get used storage in GB.