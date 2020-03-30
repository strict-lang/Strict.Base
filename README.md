# Strict.Base

The base package contains all types that have special language treatment and are required to build strict packages. It is imported
by default in every source file. 
Some of the types defined in this package are:
- Strings
- Numbers
- Slices
- Common Interfaces (Computation, Function, Sequence)

Changes to this package are done very carefully and planned, since they
will most likely impact almost every source file in the ecosystem.
Almost every type in this package is part of some special syntax.