//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[charging](charging.md)

# charging

[androidJvm]\
open fun [charging](charging.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html)&gt;

it present the Device's is charging by USB or not.

#### Return

- return in Boolean. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
if(model.charging().getValue()){
    Log.i(TAG,"user is charging the device");
}

```
model - the instance of MonkeyServiceViewModel 

call model.monkeyConnected().getValue() to check is charging or not.