# Strict.Base

The Strict Standard Library Base Package contains all types that have special language treatment and are required to build strict packages. It is imported by default in every source file.

Some of the types defined in this package are:
- Number
- Text
- List
- Range
- Error (with Stacktraces, Type and Methods support)
- Log
- common traits like Any (applies to all types), App, Generic (replaced by concrete type in implementation), Mutable, File, etc.

Changes to this package are done very carefully and planned, since they will most likely impact almost every source file in the ecosystem. By default strict code will always try to use the latest version, but if that fails will automatically fall back to the version when the type was last changed (to be in sync)

More at https://strict-lang.org

Unfinished:
- BinaryOutput with Write(bytes), which requires a Bytes type, which should be based on List(Number)
- BinaryInput with Read Bytes to load binary data back
- Plus some File and Network IO types to use with BinaryOutput and BinaryInput