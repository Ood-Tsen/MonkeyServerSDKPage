//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceViewModel](index.md)/[enableFunctions](enable-functions.md)

# enableFunctions

[androidJvm]\
open fun [enableFunctions](enable-functions.md)(functionsCommand: [FunctionsCommand](../../com.mm.monkey.server.services.enums/-functions-command/index.md), enable: [Boolean](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-boolean/index.html))

to enable or disable a single following Device's function.there are 9 types of FunctionsCommand

1. capturePhoto

2. capturePhotoByVoice

3. recordVideo

4. recordVideoByVoice

5. togglePlayback

6. skipTrack

7. adjustVolumn

8. verbalQuery

9. visualQuery

#### Return

- void 

**How to Use:**

```kotlin

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.enableFunctions(FunctionsCommand.capturePhoto,true);

```
model - the instance of MonkeyServiceViewModel. 

call model.enableFunctions to turn on a specfic FunctionsCommand,

#### Parameters

androidJvm

| | |
|---|---|
| functionsCommand | - one of FunctionsCommand. |
| enable | - true is enable. |

[androidJvm]\
open fun [enableFunctions](enable-functions.md)(list: [List](https://developer.android.com/reference/kotlin/java/util/List.html)&lt;[Pair](https://developer.android.com/reference/kotlin/android/util/Pair.html)&lt;[FunctionsCommand](../../com.mm.monkey.server.services.enums/-functions-command/index.md), [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html)&gt;&gt;)

to enable or disable a single following Device's function.there are 9 types of FunctionsCommand

1. capturePhoto

2. capturePhotoByVoice

3. recordVideo

4. recordVideoByVoice

5. togglePlayback

6. skipTrack

7. adjustVolumn

8. verbalQuery

9. visualQuery

#### Return

- void 

**How to Use:**

```kotlin

List<Pair<FunctionsCommand,Boolean>> options = new ArrayList<>();
options.add(new Pair(FunctionsCommand.capturePhoto,true));
//options.add(new Pair(FunctionsCommand.recordVideo,true));
//options.add(new Pair(FunctionsCommand.verbalQuery,true));
//options.add(new Pair(FunctionsCommand.visualQuery,true));
//options.add(new Pair(FunctionsCommand.adjustVolumn,true));
//options.add(new Pair(FunctionsCommand.capturePhotoByVoice,true));
//options.add(new Pair(FunctionsCommand.recordVideoByVoice,true));

MonkeyServiceViewModel model = MonkeyServiceViewModel.getInstance((Application)context.getApplicationContext());
model.enableFunctions(FunctionsCommand.capturePhoto,true);

```
model - the instance of MonkeyServiceViewModel. 

call model.enableFunctions to turn on a list of FunctionsCommands,

#### Parameters

androidJvm

| | |
|---|---|
| list | - list of pair with FunctionsCommand |