---
layout: post
title: First Impression of Odin
date: 2023-04-10 11:59:00-0000
description: A small breakdown of an app that I built with Odin and my half-baked opinion on the language
categories: Odin SDL Languages
disqus_comments: false
related_posts: false
---

# Odin

Odin is a language made by Gingerbil. The language is pretty new compared to the other one. I find it truly enjoyable. I considered it a little bit hipster because it doesn't follow the more mainstream concepts. This isn't a bad thing! 

## Interesting features of Odin

- Syntax is close to mathematical terminology.
- Use of UTF-8 inside the language.
- Idioms like #optional_ok and #soa enhance greatly the experience.
- Multiple returns supported as a first-class citizen
- Named parameters and returns values!
- Swizzle support for arrays
- Matrix, Quaternion supported as a first-class citizen
- `using` which gives access to internal values in the current context. This creates a behavior similar to inheritance (in some way).
- Modern Generics
- Lambda function that matches perfectly the procedure syntax declaration
- Explicit overload of function (Could be a downside for some people)
- Ginger
- Type Assertion .? .(Automatic Cast if Type is available)
- Cast and Transmutation


## External Dependencies

It was a concern at first because Odin does not come with a package manager like many modern languages. The main author of the language does not like package managers in general. He considered most of (or all of) them flawed. For this reason, it appears that a package manager will never be supported. However, because of the current build process in Odin, with git-submodule, it is pretty easy to add external library!

## Build and Compilation

Odin is more modern than C and C++ and takes advantage of modern features. The build process is simply a oneliner `odin run .` or `odin build .` and does not require external software like `CMake`. The compilation gives good-enough feedback when a syntax error has been made which make it much more accesible than C++. More could be done, but the current team is pretty small and it is already pretty impressive.

## Debugging

Debugging can be done with `lldb`. At the moment of writing this blog, the debugger is buggy.

## Assertion, Error Handling

In the current version, Odin does not support exceptions. It doesn't seem that the author wants to support this feature either. To achieve a similar result, one can use #ok_optional with a bool or an enum to return the current exception.  In fact, as he sees it, he thinks that exceptions were wrong. Those should be handled as early as possible. I was dubious at first, but by experimenting with it and #ok_optional, I saw another way to handle mistakes. A more complex experiment should be done to explore more the limitation.

## Conclusion

As you can see, Odin is very opinionated which has its benefits and issues. In the case of Odin, I would argue that he proposes interesting solutions to common issues in programming. As a very strong point for me, I'm really happy that someone gives reflection on the actual syntax/semantics. Most of the choices made felt coherent.

I truly recommend to test it to make their own opinion. As for me, for a really small project, it was a really pleasant adventure.