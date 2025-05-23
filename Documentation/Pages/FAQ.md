@page page_faq FAQ

[TOC]

# Can I disable Standard C++ Library?
Yes, if you're satisfied with the C++ standard library alternatives included in this SC and do not plan to use C++ Standard Library in your project:
- *XCode / Clang / GCC 13+*: 
    - Add **--nostdlib++**
    - Add **--nostdinc++**
- *GCC < 13*:
    - Not supported (missing **--nostdlib++**)

# Can I disable Exceptions and RTTI?
Yes, if you disable the Standard C++ Library, you can also disable Exceptions and RTTI
- *XCode / Clang / GCC*: 
    - Add **-fno-exceptions**
    - Add **-fno-rtti**
- *Visual Studio / MSVC / ClangCL*
    - Set **Enable C++ Exceptions** to **No**
    - Set **Enable Runtime Type Information** set to **No** (**GR-**)

# Does the library have debug visualizers?

Yes, this library contains debug visualizers for [Containers](@ref library_containers) and [Strings](@ref library_strings) for `clang` and `cl.exe` (Microsoft Compiler).
Using them will make your life easier.  
[Build](@ref library_build) is setting them up automatically for XCode and Visual Studio projects.

# What plans for ABI / API stability?

There are no plans to provide ABI stability.

Each library declares its own API stability, but as the project is very young, expect breaking changes for now.  
At some point API will stabilize naturally and it will be made explicit for each library.

