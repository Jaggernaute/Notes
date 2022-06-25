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

-import(io,[fwrite/1]).

%% API  
-export([say/0]).
  
say() ->  
  fwrite("Hello, World!\n").  
```

**Module declaration:**
> The `-module()` function set the module name, it should be the same as the file name without the *.erl* extension :
  So for the `./hello.erl` file the module name should be `hello` and it should be declared like `-module(hello).`.

**Function export:**
> The `-export().` function specify which of the functions are visible outside this module, it takes the function's name and the number of parameters required by said function  :
  So in the `great` module example we do `-export([say/0]).` where the function *say* which take *0* arguments is exported and can be used anywhere else in the project.

**Function import:**
> In a similar way the `-import().` function is used to import functions that are exported by others libraries. It takes the *module name* from which is exported the function and the same `[name/param]` as the export :
  So in order to use the `fwrite().` function we need to import it from the *io* module, like so: `-import(io,[fwrite/1]).`.

**Dot symbol**
> Note that every *statement* is delimited by a dot **.** symbol. Each statement need that *delimiter*, **but not every line**.

**Comments**
> *Comments* are declared with the **%** symbol. And *doc-strings* are declared with two of those like `%% @author jaggernaute`. and for file *headers* I like to use thin syntax :
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