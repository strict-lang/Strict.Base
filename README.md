# Strict.Base

The Strict Standard Library Base Package contains all types that have special language treatment and are required to build strict packages. It is imported by default in every source file.

Some of the types defined in this package are:
- Boolean
- Number
- Text
- List
- Dictionary
- Range
- Error (with Stacktraces, Type and Methods support)
- Log
- common traits like Any (applies to all types), App, Generic (replaced by concrete type in implementation), Mutable, File, Directory, FileReader, FileWriter, etc.

That is pretty much it, there are not many more things needed to write code. For more specific things like Math types, Image processing, etc. there are some other projects, but keep in mind that Strict is NOT a general purpose language. It is supposed to be writeable, readable and understandable by computers. If you want to build a website, a complex app, database code, a game, etc. you should use external code for that (you can keep the logic in Strict, but it is unlikely that Strict will have those things unless some people work on it and need it). It is quite easy to interface with external code, you can use any web api, C++, C#, Java, Python, etc. libraries. Those are threated as black boxes (thus not longer computer understandable, here we would be limited to LLMs) and will not follow the strict rules in Strict. The main issue here would be if an external library changes, then all your calls to it also have to change, which is less of a problem with Strict code calling Strict code as any changes can be fixed in a more automated manner.

Changes to this package are done very carefully and planned, since they will most likely impact almost every source file in the ecosystem. By default strict code will always try to use the latest version, but if that fails will automatically fall back to the version when the type was last changed (to be in sync, using git )

More at https://strict-lang.org

# How to use
The best way to learn how any expression or base type works is to look at the code, it is very compact and every single method starts with tests on how to use it. This base library is not just defining how the language works, but the documentation in source code form. All tests use the is comparsion (similar to == in c style languages, = is used for assignments), "is true" at the end of any expression is never used. All expressions (not just tests) must evaluate to true, otherwise the execution stops with an error. If an expression is constant (like all tests, but also many other expressions), it will be removed and optimized out after the first run.

See the Readme.md of the Strict project for more details, how to use and example code.