# **Allocate**




Terra System System allocate [Memory](../../../Execute/System/Memory/a.md) to execute Module.



Memory available to Module is in Memory Block list.
Memory Block is in 2^16 byte size.



Terra System System allocate Memory to make Object when Object is not store in refer to it.



Memory allocate to [Object](../../../Class/Object/a.md) is consist of all field data of class derive,
Int A, Int B, Int C, Int D.
Memory is continue in byte for all data to allocate.
All Memory space is available in 1 allocate.





Int A is refer count from any Object.


Int B is refer count from any Object in refer graph of free.


Int C is next refer of link list of Object root that has Int A and Int B not equal.


Int D has flag A that is traverse before in refer graph, has flag B that is in refer graph of any Object root that has Int A and Int B not equal.





Object N data Int A is add 1 when a field of Object is set from not refer to N to refer to N.
Int A is sub 1 when a field of Object is set from refer to N to not refer to N.




Refer graph is traverse by check Int D flag A, if 1, not traverse again.
Object A is traverse by link current tail Object B Int C to refer to Object A.




When Object N data Int A is 0, refer graph from Object N is traverse to set Int B, Int C 0, set Int D flag B 0 for all Object in graph.

Refer graph is traverse again to add Int B by 1 for refer by Object in graph.

Refer graph is traverse again to link list all Object that has Int A and Int B not equal by set Int C to refer to next Object.

Link list is iter with Int C to traverse refer graph each root that is Object in list to set all Object in the refer graph list Int D flag B to 1.

Refer graph root of Object N is traverse again to free Memory of all Object that has Int D flag B 0.




Allocate Memory consist of Terra Op List.
Traverse refer graph consist of Terra Op List.
Free Memory consist of Terra Op List.