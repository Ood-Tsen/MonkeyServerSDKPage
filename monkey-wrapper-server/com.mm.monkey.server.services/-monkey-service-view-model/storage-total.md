//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[storageTotal](storage-total.md)

# storageTotal

[androidJvm]\
open fun [storageTotal](storage-total.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Double](https://developer.android.com/reference/kotlin/java/lang/Double.html)&gt;

it present the Device's total storage in GB.

#### Return

- return in Double. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
Log.i(TAG," the total storage is " + model.storageTotal().getValue() + " GB");

```
model - the instance of MonkeyServiceViewModel 

call model.storageTotal().getValue() to get total storage in GB.