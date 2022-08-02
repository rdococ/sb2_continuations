Scriptblocks 2 Continuations
============================

An extension to [Scriptblocks 2](https://github.com/rdococ/scriptblocks2) that adds first-class continuations. First-class continuations were originally an experimental feature of Scriptblocks 2 that has since been removed. This mod readds them.

## Notice

This mod is for compatibility purposes with previous Scriptblocks 2 versions, and to test the viability of extensions. For new projects, you should use the coroutines built into Scriptblocks 2 instead.

## Features

* First-class, multi-shot undelimited continuations with "Call/CC", "Invoke Continuation".
* First-class, multi-shot, multi-prompt delimited continuations with "Call With Continuation Delimiter", "Call With Delimited Continuation".

The delimited continuation operators are designed to act like reset0/shift0. A "shift0" nested within a "shift0" will not be delimited by the corresponding "reset0", but invoking the corresponding delimited continuation will reinstate the "reset0".