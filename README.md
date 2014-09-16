TyPack
======

Efficiently typed serialization format (in the spirit of [Msgpack][1]).

[Msgpack][1] is a great serialization format, but it suffers serveral drawbacks:

* No support for structs. Has to be encoded as array or map.
* Has to encode type information for every value. There is no such thing as an array of uint8's.
* No (optional) typing information on structs or struct fields.
* The two versions of the specs are somewhat incompatible. Handling of String and Binary.
* It never got support for unsized arrays or structs, i.e. the size has to be know up-front.
* IMHO, especially for maps and arrays, it tries too provide too many variants. For an array with more than 256 values, it should
  be ok, to spend two more bytes.

TyPack tries to overcome many of these shortcomings while being very similar in both the serialization format used and the 
philosophy of msgpack.

[1]: http://www.msgpack.org/
