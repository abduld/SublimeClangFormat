Clang Format
============

What it does
------------
Clang-format is a tool for re-formatting C++, built on llvm. This is a
package that allows you to run it easily from within Sublime Text.

![demo](https://raw.githubusercontent.com/rosshemsley/demos/master/clang_format.gif)

About
-----
In this package, we provide an alternative wrapper around clang-format
for use within Sublime Text 3. Whilst llvm does provide a very simple plugin
to work with Sublime Text already:
https://llvm.org/svn/llvm-project/cfe/trunk/tools/clang-format/clang-format-sublime.py,
it doesn't really exploit any of the Sublime Text package functionality. 
We add new features such as customising the style from a settings file,
selecting styles using the Command Palette, and easier installation.

Installing
----------
- Install this package through Package Control in the usual way.
- Get the clang-format binary. If you don't already have it, you can download
  binaries from llvm: http://llvm.org/releases/download.html.
  This will give you the whole llvm toolchain... however, for the philistines
  among you: yes, it appears you can just copy the binary for clang-format
  out of the bin directory and trash the rest and it will still work.
- Set the path to the clang-format binaries. You can do this from within Sublime
  Text by choosing `Clang Format - Set Path` from the command palette.  Hint: 
  the path should look something like this `[path/to/clang]/clang/bin/clang-format`.
  If clang-format is in your system path, you shouldn't need to do anything.

Use
---
- Default shortcut is `super+option+a` on OSX and `ctrl+option+a` otherwise.
  This will apply clang-format to the selection.
- From the command palette, you can select the formatting type by using
  `Clang Format: Select Style`. You will find the small number of defaults,
  and also a new 'Custom' entry. Selecting this entry allows you to customise
  the style through a settings file. You can access it from the main menu,
  under `Package Settings`. In this file you can add custom rules, such 
  as `Allmen` style braces, and different indents. For examples see
  http://clang.llvm.org/docs/ClangFormatStyleOptions.html.
- Settings for the 'Custom' format and others are available through the Sublime
  Text preferences. Note that it is possible to enable the formatter on every
  save to a C/C++ file. To change settings on a per-package basis, check out the
  package "Project-Specific".

If You Liked This
-----------------
If you like this plugin, maybe you'll like my other plugin, iOpener. It makes
opening files significantly easier and will feel completely natural if you're
used to using a shell. Otherwise, why not pop over and star this repo on GitHub?

Credits
-------
Thanks to the llvm project for doing the hard work, including writing clang
format, and also the original Sublime Text plugin on which this package is
based.

Also, why not go and watch the video that got me interested in clang-format in
the first place?

http://channel9.msdn.com/Events/GoingNative/2013/The-Care-and-Feeding-of-C-s-Dragons
