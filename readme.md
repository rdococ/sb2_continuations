Scriptblocks 2 Continuations
============================

An extension to [Scriptblocks 2](https://github.com/rdococ/scriptblocks2) that adds first-class continuations. First-class continuations were originally an experimental feature of Scriptblocks 2 that has since been removed. This mod readds them.

## Warning

If you don't understand what "first-class delimited continuation" means, you don't need this mod. Use Scriptblocks 2's coroutines - pausable closures which are just as powerful while being simpler to understand.

This is for compatibility purposes, and to test the viability of Scriptblocks 2 extensions. Scriptblocks 2 offers cloneable coroutines which are equivalent to multi-shot, single-prompt delimited continuations, which can implement multi-prompt continuations.

## Features

* First-class, multi-shot undelimited continuations with "Call/CC", "Invoke Continuation".
* First-class, multi-shot, multi-prompt delimited continuations with "Call With Continuation Delimiter", "Call With Delimited Continuation".

The delimited continuation operators are designed to act like reset0/shift0. A "shift0" nested within a "shift0" will not be delimited by the corresponding "reset0", but invoking the corresponding delimited continuation will reinstate the "reset0". This behaviour is akin to re-resumable exceptions or cloneable coroutines.