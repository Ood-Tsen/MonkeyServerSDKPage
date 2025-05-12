//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[monkeyConnected](monkey-connected.md)

# monkeyConnected

[androidJvm]\
open fun [monkeyConnected](monkey-connected.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html)&gt;

it presend CA and 3rd app is binded or not. All properties and functions should be ready after monkeyConnected is true.

#### Return

- return in Boolean. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
if(model.monkeyConnected().getValue()){
    model.getDeviceInfo();
}

```
model - the instance of MonkeyServiceViewModel 

call model.monkeyConnected().getValue() to check is bind or not.