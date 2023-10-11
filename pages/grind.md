- can use keyword like so:
	- `grind :exclude "^^"`
	- this will exclude the definition of ^^ (non-natural [[exponentiation]]) from the expansions that happen when you `grind`
- dangerous command, does a bunch of definition expansion and [[instantiation]]
- can take a long time, never stop, or reach some weird conclusions
- ex. `(grind :exclude "arg")` [[grind]]
  collapsed:: true
	- [[grind]] expands the definitions of things like crazy
	  collapsed:: true
		- the definition of non-natural [[exponentiation]] is complicated,
		- exclude ensures [[grind]] doesn't [[expand]] it
	- ex. used in `dl-diffghost` example in nasalib [[ghosts]]
