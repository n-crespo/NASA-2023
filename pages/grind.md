Grind
=====
- can use keyword like so:
	- `grind :exclude "^^"`
  - this will exclude the definition of ^^ (non-natural [exponentiation](exponentiation.md)) from the expansions that happen when you `grind`
- dangerous command, does a bunch of definition expansion and [instantiation](pages/instantiation.md)
- can take a long time, never stop, or reach some weird conclusions
- ex. `(grind :exclude "arg")`
	- grind expands the definitions of things like crazy
		- the definition of non-natural exponentiation is complicated,
    - exclude ensures grind doesn't [expand](pages/expand.md) it
	- used in `dl-diffghost` example in nasalib
