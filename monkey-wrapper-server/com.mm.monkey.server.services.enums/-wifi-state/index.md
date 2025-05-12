//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services.enums](../index.md)/[WifiState](index.md)

# WifiState

[androidJvm]\
enum [WifiState](index.md)

## Entries

| | |
|---|---|
| [UNKNOWN_STATE](-u-n-k-n-o-w-n_-s-t-a-t-e/index.md) | [androidJvm]<br>[UNKNOWN_STATE](-u-n-k-n-o-w-n_-s-t-a-t-e/index.md) |
| [DISCONNECTED](-d-i-s-c-o-n-n-e-c-t-e-d/index.md) | [androidJvm]<br>[DISCONNECTED](-d-i-s-c-o-n-n-e-c-t-e-d/index.md) |
| [CONNECTING](-c-o-n-n-e-c-t-i-n-g/index.md) | [androidJvm]<br>[CONNECTING](-c-o-n-n-e-c-t-i-n-g/index.md) |
| [CONNECTED](-c-o-n-n-e-c-t-e-d/index.md) | [androidJvm]<br>[CONNECTED](-c-o-n-n-e-c-t-e-d/index.md) |
| [DISCONNECTING](-d-i-s-c-o-n-n-e-c-t-i-n-g/index.md) | [androidJvm]<br>[DISCONNECTING](-d-i-s-c-o-n-n-e-c-t-i-n-g/index.md) |

## Properties

| Name | Summary |
|---|---|
| [description](description.md) | [androidJvm]<br>open val [description](description.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html) |
| [state](state.md) | [androidJvm]<br>open val [state](state.md): [Int](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-int/index.html) |

## Functions

| Name | Summary |
|---|---|
| [fromOri](from-ori.md) | [androidJvm]<br>open fun [fromOri](from-ori.md)(state: [Int](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-int/index.html)): [WifiState](index.md) |
| [valueOf](value-of.md) | [androidJvm]<br>open fun [valueOf](value-of.md)(name: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [WifiState](index.md)<br>Returns the enum constant of this type with the specified name. The string must match exactly an identifier used to declare an enum constant in this type. (Extraneous whitespace characters are not permitted.) |
| [values](values.md) | [androidJvm]<br>open fun [values](values.md)(): [Array](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-array/index.html)&lt;[WifiState](index.md)&gt;<br>Returns an array containing the constants of this enum type, in the order they're declared. This method may be used to iterate over the constants. |