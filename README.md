monotouch-binding-generator
===========================

MonoMac contains a parser that can generates MonoTouch bindings from Objective C headers.  
It's far from perfect but it's a good starting point nevertheless.

I created this repository to avoid checking out monomac and maccore and maybe tweak the parser a little.  
Right now this project just puts together two files from MonoMac codebase:

* https://raw.github.com/mono/monomac/master/src/parse.cs
* https://raw.github.com/mono/maccore/master/src/Options.cs

To compile it, run

    gmcs *.cs -out:parse.exe

To use the parser, feed it your ObjC headers:

    mono parse.exe GSFancyTextView.h

That's it!
