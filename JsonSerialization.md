# JsonSaveGame

1.Enable Plugin

<img width="745" height="110" alt="image" src="https://github.com/user-attachments/assets/adf30f86-11c3-4c89-a5b7-4314aadea1e2" />

2.How to use

<img width="748" height="411" alt="image" src="https://github.com/user-attachments/assets/bb10aeb3-4219-4b03-a2e2-d2962064f3a7" />

<img width="498" height="580" alt="image" src="https://github.com/user-attachments/assets/d59cdf75-4579-49bf-b7e6-6231fdec8e85" />

<img width="242" height="56" alt="image" src="https://github.com/user-attachments/assets/14ae77a8-398e-4dc5-9728-8e6d72a08468" />

<img width="292" height="202" alt="image" src="https://github.com/user-attachments/assets/0e359693-49d5-4b81-b617-bf2afd3532c6" />


3.Limitations and known issues

(1).The logic for creating a UObject is very complex, so the plugin will not automatically create a UObject.

When SerializeObjectToJson is called, if a UObject member variable sets SaveGame and it is valid, it will be saved as JsonObject.

When DeserializeJsonToObject is called, if it is valid, read the data from JsonObject; otherwise, skip it.

Alternatively, you can create it later, then look up the data from the Json and call DeserializeJsonToObject.

创建UObject的逻辑十分的复杂，所以插件不会自动创建UObject

当调用SerializeObjectToJson时，如果一个UObject成员变量设置了SaveGame，如果它是有效的，它将被保存为JsonObject。

当调用DeserializeJsonToObject时，如果它是有效的，就从JsonObject读取数据，否则就跳过它。

或者，你可以之后再创建它，然后从Json中查找数据，再调用DeserializeJsonToObject。

(2).Similarly, when using container types (TArray, TMap, TSet), there are also some limitations if UObject is used.

First of all, none of them will automatically create UObjects. You have to create them yourself.

TArray:If the index exists in the array, it will be deserialized for it; otherwise, it will be skipped.

TSet:If UObject is used, it will be skipped directly. You must create and deserialize them yourself.

TMap:

If the Key exists, it will be deserialized for it; otherwise, it will be skipped.

You cannot use UObject as the Key, it will be skipped.

If a struct is used as the Key, although this is not a good idea, it will still be serialized into a JsonString. There is no guarantee that doing this will be fine. It is experimental.

同样的，使用容器类型时（TArray、TMap、TSet），如果使用UObject也有一些限制。

首先，它们都不会自动创建UObject，你必须自己创建它们。

TArray:如果索引在数组中存在，则会为它进行反序列化，否则跳过它

TSet:如果使用UObject会直接跳过。你必须自己创建并反序列化它们。

TMap:

如果Key存在，则会为它进行反序列化，否则跳过它。

你不能用UObject当Key。

如果用结构体当Key，虽然这不是一个好注意，但是它还是会被序列化为一个JsonString。不能保证这么做没问题，它是实验性的。
