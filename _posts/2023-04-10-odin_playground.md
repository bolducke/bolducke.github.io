---
layout: post
title: Playing with Odin
date: 2023-04-10 11:59:00-0000
description: A small breakdown of an app that I built with Odin and my half-baked opinion on the language
categories: Odin SDL Languages
disqus_comments: false
related_posts: false
---

[source code](https://github.com/bolducke/OOBC)

## Odin

Odin is a new language made by Gingerbil. The language is pretty new compare to other one. I find it truly enjoyable. I considered it a little bit hipster because it doesn't follow mainstream concept. This isn't a bad thing! 

### Interesting feature of Odin

- Syntax is close to mathematical terminology.
- Use of UTF-8 inside the language.
- Idioms like #optional_ok and #soa that enhance greatly the experience.
- Multiple returns supported as a first class citizen
- Named parameters and returns values!
- Swizzle support for arrays
- Matrix, Quaternion supported as first class citizen
- `using` which give access to internal values to the current context. This create a behavior similar to inheritance (in some way).
- Modern Generics
- Lambda function that match perfectly the procedure syntax declaration
- Explicit overload of function (Could be a downside for some people)
- Ginger
- Type Assertion .? .(Automatic Cast if Type is available)
- Cast and Transmutation


### External Dependencies

This was a concern at first because Odin do not come with a package manager like many modern language. I am traumatized how it was hard to integrate existing library into project some time (I'm talking about you OpenCV). The main author of the language do not like package manager in general. He considered most of (or all of) them flawed. For this reason, it appear that package manager will never be supported as for rust, python, etc. However, because of the current build process in Odin, with gitsubmodule, it is pretty easy to add external library!

### Build and Compilation

Odin is more modern than C and C++ and take advantages of modern features. The build process is simply a oneliner `odin run .` or `odin build .` and do not require external software or manual labor to link external dependencies. At the same time, compilation time are fast. Compilation give interesting feedback when obvious mistake are done which accelerate the creative process. More could probably been done, but the current team is pretty small and it is already pretty impressive.

### Debugging

Debugging can be done with `lldb`, but it is limited. There is still many issues with the current implementation. 

### Assertion, Error Handling

In the current version, Odin do not support exception. It doesn't seem that the author want to support this feature neither. To achieve similar result, one can use #ok_optional with a bool or an enum to return the current exception. 
In fact, as he see it, he thinks that exception were wrong. Those should be handle as fast as possible. I was dubious at first, but by experimenting with it and #ok_optional, I saw another way to handle mistake. More complex program should be done to experiment with the current process.

### Conclusion

As you can see, Odin is very opionated which have his benefits and issues. In the case of Odin, I would argue that he propose interesting solutions to common issues in programming. As a very strong to point for me, I'm really happy that someone give enough reflection on the actual syntax/semantics. Most of them are coherent. It's very neat that procedure inside a function or outside keep the same syntax.

I truly recommend one to test it to make their own opinion. As for me, for a really small project, this was pleasant.