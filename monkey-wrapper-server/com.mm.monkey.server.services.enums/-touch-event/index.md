//[monkeyWrapperServer](../../../index.md)/[com.mm.monkey.server.services.enums](../index.md)/[TouchEvent](index.md)

# TouchEvent

[androidJvm]\
enum [TouchEvent](index.md)

## Entries

| | |
|---|---|
| [ONE_TAP](-o-n-e_-t-a-p/index.md) | [androidJvm]<br>[ONE_TAP](-o-n-e_-t-a-p/index.md) |
| [DOUBLE_TAP](-d-o-u-b-l-e_-t-a-p/index.md) | [androidJvm]<br>[DOUBLE_TAP](-d-o-u-b-l-e_-t-a-p/index.md) |
| [TRIPPLE_TAP](-t-r-i-p-p-l-e_-t-a-p/index.md) | [androidJvm]<br>[TRIPPLE_TAP](-t-r-i-p-p-l-e_-t-a-p/index.md) |
| [SWIPE_FORWARD](-s-w-i-p-e_-f-o-r-w-a-r-d/index.md) | [androidJvm]<br>[SWIPE_FORWARD](-s-w-i-p-e_-f-o-r-w-a-r-d/index.md) |
| [SWIPE_BACKWARD](-s-w-i-p-e_-b-a-c-k-w-a-r-d/index.md) | [androidJvm]<br>[SWIPE_BACKWARD](-s-w-i-p-e_-b-a-c-k-w-a-r-d/index.md) |
| [SWIPE_UP](-s-w-i-p-e_-u-p/index.md) | [androidJvm]<br>[SWIPE_UP](-s-w-i-p-e_-u-p/index.md) |
| [SWIPE_DOWN](-s-w-i-p-e_-d-o-w-n/index.md) | [androidJvm]<br>[SWIPE_DOWN](-s-w-i-p-e_-d-o-w-n/index.md) |
| [UNKNOWN_EVENT](-u-n-k-n-o-w-n_-e-v-e-n-t/index.md) | [androidJvm]<br>[UNKNOWN_EVENT](-u-n-k-n-o-w-n_-e-v-e-n-t/index.md) |

## Properties

| Name | Summary |
|---|---|
| [description](description.md) | [androidJvm]<br>open val [description](description.md): [String](https://developer.android.com/reference/kotlin/java/lang/String.html) |
| [event](event.md) | [androidJvm]<br>open val [event](event.md): [Int](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-int/index.html) |

## Functions

| Name | Summary |
|---|---|
| [fromOri](from-ori.md) | [androidJvm]<br>open fun [fromOri](from-ori.md)(touch_event: [Int](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-int/index.html)): [TouchEvent](index.md) |
| [valueOf](value-of.md) | [androidJvm]<br>open fun [valueOf](value-of.md)(name: [String](https://developer.android.com/reference/kotlin/java/lang/String.html)): [TouchEvent](index.md)<br>Returns the enum constant of this type with the specified name. The string must match exactly an identifier used to declare an enum constant in this type. (Extraneous whitespace characters are not permitted.) |
| [values](values.md) | [androidJvm]<br>open fun [values](values.md)(): [Array](https://kotlinlang.org/api/core/kotlin-stdlib/kotlin/-array/index.html)&lt;[TouchEvent](index.md)&gt;<br>Returns an array containing the constants of this enum type, in the order they're declared. This method may be used to iterate over the constants. |