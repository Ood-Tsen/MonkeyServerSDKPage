//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[language](language.md)

# language

[androidJvm]\
open fun [language](language.md)(): [LiveData](https://developer.android.com/reference/kotlin/androidx/lifecycle/LiveData.html)&lt;[Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html)&gt;

it present the Device's voice trigger language.

#### Return

- return in Locale. 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
Log.i(TAG," the AI language is " + model.language().getValue());

```
model - the instance of MonkeyServiceViewModel 

call model.language().getValue() to get total storage in GB.