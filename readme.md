# TrueDllInjection

A project for properly injecting C++ and C# dlls into other processes.

## Rationale

While merely getting your custom dll injected into a target process' memory
space is fun, it is only half of the story. Most dll injection tutorials will
describe in detail the first half, but then leave you to run your code from
within DllMain, a dangerous and limited proposition. For more information about
why you should avoid doing anything interesting in your DllMain, read
[this thread](http://blogs.msdn.com/b/oldnewthing/archive/2004/01/27/63401.aspx)
by Raymond Chen.

This project aims to change that dearth of good dll-injection info, providing an
open-source way of not only injecting a dll, but also walking the export address
table and calling a method on your dll.

This project is specifically geared towards injecting managed code into another
process. We will first inject the "Bootstrapper" module, then tell it to load
the CLR and start our example managed project.

## License

TODO
