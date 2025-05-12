//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services](../index.md)/[MonkeyServiceProxy](index.md)/[getDescription](get-description.md)

# getDescription

[androidJvm]\
open fun [getDescription](get-description.md)(locale: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [String](https://developer.android.com/reference/kotlin/java/lang/String.html)

getDescription check permission defined in the Annotation 'Permission' of the function MonkeyClient.getDescription

#### Return

, the Sting of description 

**How to Use:**

```kotlin

// after extend from MonkeyServiceProxy
public String getDescription(String locale) throws RemoteException {

   return "This service is for monkey.";
}

```

#### Parameters

androidJvm

| | |
|---|---|
| locale | en-US also. |