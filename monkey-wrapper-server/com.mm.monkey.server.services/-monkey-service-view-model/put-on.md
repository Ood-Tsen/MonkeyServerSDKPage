//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[putOn](put-on.md)

# putOn

[androidJvm]\
open fun [putOn](put-on.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html)&gt;

it presend user put on or take off the Device(Glasses).

#### Return

- return in Boolean 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.putOn().observeForever(put_on->{
    if(put_on) Log.i(TAG,"user put on device");
}

```
model - the instance of MonkeyServiceViewModel 

call model.putOn() to get liveData and observe it. 

while observed, do the following actions.