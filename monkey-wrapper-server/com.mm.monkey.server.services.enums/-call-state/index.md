//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services.enums](../index.md)/[CallState](index.md)

# CallState

[androidJvm]\
enum [CallState](index.md)

## Entries

| | |
|---|---|
| [CALL_STATE_UNKNOWN](-c-a-l-l_-s-t-a-t-e_-u-n-k-n-o-w-n/index.md) | [androidJvm]<br>[CALL_STATE_UNKNOWN](-c-a-l-l_-s-t-a-t-e_-u-n-k-n-o-w-n/index.md) |
| [CALL_STATE_ACTIVE](-c-a-l-l_-s-t-a-t-e_-a-c-t-i-v-e/index.md) | [androidJvm]<br>[CALL_STATE_ACTIVE](-c-a-l-l_-s-t-a-t-e_-a-c-t-i-v-e/index.md) |
| [CALL_STATE_HELD](-c-a-l-l_-s-t-a-t-e_-h-e-l-d/index.md) | [androidJvm]<br>[CALL_STATE_HELD](-c-a-l-l_-s-t-a-t-e_-h-e-l-d/index.md) |
| [CALL_STATE_DIALING](-c-a-l-l_-s-t-a-t-e_-d-i-a-l-i-n-g/index.md) | [androidJvm]<br>[CALL_STATE_DIALING](-c-a-l-l_-s-t-a-t-e_-d-i-a-l-i-n-g/index.md) |
| [CALL_STATE_ALERTING](-c-a-l-l_-s-t-a-t-e_-a-l-e-r-t-i-n-g/index.md) | [androidJvm]<br>[CALL_STATE_ALERTING](-c-a-l-l_-s-t-a-t-e_-a-l-e-r-t-i-n-g/index.md) |
| [CALL_STATE_INCOMING](-c-a-l-l_-s-t-a-t-e_-i-n-c-o-m-i-n-g/index.md) | [androidJvm]<br>[CALL_STATE_INCOMING](-c-a-l-l_-s-t-a-t-e_-i-n-c-o-m-i-n-g/index.md) |
| [CALL_STATE_WAITING](-c-a-l-l_-s-t-a-t-e_-w-a-i-t-i-n-g/index.md) | [androidJvm]<br>[CALL_STATE_WAITING](-c-a-l-l_-s-t-a-t-e_-w-a-i-t-i-n-g/index.md) |
| [CALL_STATE_HELD_BY_RESPONSE_AND_HOLD](-c-a-l-l_-s-t-a-t-e_-h-e-l-d_-b-y_-r-e-s-p-o-n-s-e_-a-n-d_-h-o-l-d/index.md) | [androidJvm]<br>[CALL_STATE_HELD_BY_RESPONSE_AND_HOLD](-c-a-l-l_-s-t-a-t-e_-h-e-l-d_-b-y_-r-e-s-p-o-n-s-e_-a-n-d_-h-o-l-d/index.md) |
| [CALL_STATE_TERMINATED](-c-a-l-l_-s-t-a-t-e_-t-e-r-m-i-n-a-t-e-d/index.md) | [androidJvm]<br>[CALL_STATE_TERMINATED](-c-a-l-l_-s-t-a-t-e_-t-e-r-m-i-n-a-t-e-d/index.md) |

## Properties

| Name | Summary |
|---|---|
| [description](description.md) | [androidJvm]<br>open val [description](description.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html) |
| [state](state.md) | [androidJvm]<br>open val [state](state.md): [Int](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-int/index.html) |

## Functions

| Name | Summary |
|---|---|
| [fromOri](from-ori.md) | [androidJvm]<br>open fun [fromOri](from-ori.md)(call_state: [Int](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-int/index.html)): [CallState](index.md) |
| [valueOf](value-of.md) | [androidJvm]<br>open fun [valueOf](value-of.md)(name: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [CallState](index.md)<br>Returns the enum constant of this type with the specified name. The string must match exactly an identifier used to declare an enum constant in this type. (Extraneous whitespace characters are not permitted.) |
| [values](values.md) | [androidJvm]<br>open fun [values](values.md)(): [Array](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-array/index.html)&lt;[CallState](index.md)&gt;<br>Returns an array containing the constants of this enum type, in the order they're declared. This method may be used to iterate over the constants. |