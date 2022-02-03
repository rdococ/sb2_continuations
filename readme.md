Scriptblocks 2 Continuations
============================

An extension to [Scriptblocks 2](https://github.com/rdococ/scriptblocks2) that readds first-class continuations.

**This is for compatibility purposes, and to test the viability of Scriptblocks 2 extensions. Scriptblocks 2 offers cloneable coroutines which have the same expressive power as delimited continuations.**

## Features

* First-class undelimited continuations with "Call/CC", "Invoke Continuation".
* First-class delimited continuations with "Call With Continuation Delimiter", "Call With Delimited Continuation".

The delimited continuation operators are designed to act like reset0/shift0. "shift0" nested within "shift0" will not be delimited by the corresponding "reset0", but invoking the corresponding delimited continuation will reinstate the "reset0". This behaviour is akin to re-resumable exceptions or cloneable coroutines.