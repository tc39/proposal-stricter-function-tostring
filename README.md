# Stricter Function.prototype.toString

## Status

* Champion(s): Richard Gibson
* Stage: 0

## Motivation

The
[Function.prototype.toString revision proposal](https://github.com/tc39/Function-prototype-toString-revision)
and its
[needs-consensus followup commit](https://github.com/tc39/ecma262/commit/552407b105696bafa4e641bf2f5db61ad39c65ab)
went a long way in constraining the output of `Function.prototype.toString` for
built-in functions and other functions for which no source text representation
is available, but left some implementation flexibility with respect to
whitespace and the contents of that output taking the place of a function name.
But the entire ecosystem benefits from uniformity across implementations, so
such flexibility does not seem beneficial.
This proposal is an attempt to impose further constraints and corresponding
predictability.
We do not have a preference regarding any particular representation, and are
willing to negotiate with implementations as necessary.

<!--
## Use cases

**Use case 1**: description
-->

## Description

If adopted, this proposal will reduce implementation flexibility regarding the
output of `Function.prototype.toString` that is described by the
[NativeFunction](https://tc39.es/ecma262/multipage/fundamental-objects.html#prod-NativeFunction) 
production (e.g., for built-in functions, bound functions, and proxied
functions).
The scope specifically includes whitespace, tokens in between `function` and
`(`, and the syntactically invalid body, and may expand to include the parameter
list as well.
  
<!--
## Comparison 
-->
  
## Implementations
 
There are no known implementations.

<!--
### Polyfill/transpiler implementations

### Native implementations

- [V8]() (*Links to tracking issues in each JS engine*)
- [JSC]()
- [SpiderMonkey]()
- ...
-->

<!--
## Q&A

**Q**: Why is the proposal this way?

**A**: Because reasons!
-->
