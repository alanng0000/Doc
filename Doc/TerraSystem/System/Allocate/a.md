# **Allocate**




Terra System System allocate [Memory](../../../Execute/System/Memory/a.md) to execute Module.



Memory available to Module is in Memory Block list.
Memory Block is in 2^16 byte size.



Terra System System allocate Memory to make Object when Object is not stored in refer to it.



Memory allocate to [Object](../../../Class/Object/a.md) is consist of all field data of class derive,
Int A, Int B.
Memory is continue in byte for all data to allocate.
All data is allocate in 1 time.





Int A is refer count from any Object.


Int B is refer count from any Object in refer graph of free.



Object N data Int A is add 1 when a field of Object is set from not refer to N to refer to N.
Int A is sub 1 when a field of Object is set from refer to N to not refer to N.


When Object N data Int A is 0, refer graph from Object N is traverse to set Int B 0 for all Object in graph.
Refer graph is traverse again to add Int B by 1 for refer by Object in graph.
Refer graph is traverse again to free all Object that has Int A and Int B equal.


Allocate Memory consist of Terra Op.
Traverse refer graph consist of Terra Op.
Free Memory consist of Terra Op.