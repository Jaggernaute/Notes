# ![memo](https://github.githubassets.com/images/icons/emoji/unicode/1f4dd.png) Erlang notes
---

Erlang is a *functional* programming language, it has it's own *runtime environment*.

Erlang should be used to develop your application, if you have the following requirements :
- The application needs to handle a *large number of concurrent activities*.

- It should be *easily distributable* over a *network of computers*.

- There should be a facility to make the application *fault-tolerant* to both *software and hardware errors*.

- The application should be *scalable*. This means that it should have the ability to span across *multiple servers* with *little or no change*.
   
- It should be *easily upgradable* and *reconfigurable* without having to *stop and restart* the application itself.
 
- The application should be responsive to users within *certain strict timeframes*.

---

# Hello world program :

```erlang
-module(great).  
-author("jaggernaute").  
  
%% API  
-export([hello/0]).  
  
say() ->  
  io:fwrite("Hello, World!\n").  
```

> The `-module()` is the module name, it should be the same as the file name without the *.erl* extension :
  So for the `./hello.erl` file the module name should be `hello` and it should be declared like `-module(hello).`.

> In a similar way the `-export().` 

> Note that every statement is delimited by a dot **.** symbol. Each statement need that delimiter, **but not every line**.

> Comments are declared with the **%** symbol. And doc-strings are declared with two of those like `%% @author jaggernaute`. and for file headers I like to use thin syntax :
```erlang 
%%%-------------------------------------------------------------------  
%%% @author jaggernaute  
%%% @copyright (C) 2022, JaggerCorp  
%%% @doc  
%%%  some really interesting doc
%%% @end  
%%% Created : 23. Jun 2022 11:58 PM  
%%%-------------------------------------------------------------------
```

---
## Links and tags
Here are the links to others obsidians notes (even if the appear before )
[[CS Introduction]]
#erlang #Computer-science #programming 