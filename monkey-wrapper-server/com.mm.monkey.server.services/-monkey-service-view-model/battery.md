//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[battery](battery.md)

# battery

[androidJvm]\
open fun [battery](battery.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html)&gt;

it present the Device's battery level from 0 to 100.

#### Return

- return in Integer. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
if(model.battery().getValue() < 30){
    Log.i(TAG," the device battery level is less than 30%");
}

```
model - the instance of MonkeyServiceViewModel 

call model.battery().getValue() to get the battery level.