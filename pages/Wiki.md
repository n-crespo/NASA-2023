Wiki
====
# Table of Contents 
1. [First do this](#first-do-this)
2. [Intro to PVS](#intro-to-pvs)
   * [Variables and Constants](#variables-and-constants)
3. [Writing things in PVS and dL](#writing-things-in-pvs-and-dl)
4. [Proving things in PVS and dL](#proving-things-in-pvs-and-dl)
   * [Miscellaneous](#miscellaneous)
   * [Simplification](#simplification)
   * [Utilities](#utilities)
   * [dL Commands](#dl-commands)
5. [Differential Equations, Ghosts and Invariants](#differential-equations,-ghosts-and-invariants)
6. [Off-Topic Math](#off-topic-math)

# Intro
- theres not a lot of documentation on dL compared to PVS
- André Platzer basically made the whole concept and made a paywalled book about it
  - I have pdf version
  - he also has recorded lectures on each chapter of his textbook for free on youtube
  - "Logical Foundations of Cyber Physical Systems"
- dL is an embedding inside PVS
  - it has its own mini turnstile and own Commands (`dl-command`)
  - it is not the same as PVS
  - think of it as a small piece
- pretty simple things I've modeled and/or proved:
  - newton's law of cooling 
  - example of a Bernoulli equation
  - population growth differential equation
  - bang bang controller 
  - two cars following each other 
- "step through" an already solved proof (in vscode-pvs) by clicking prove, then clicking the arrows in the small window in the bottom left
- if image becomes unresponsive 
  - click settings icon in the top left, ensure that cmd is mapped to the "meta" key, hit cmd, and click the window you want to focus
  - alternatively, click the second icon from the left on the top of the image, which opens an app switcher
  - note: if you don't want the meta key to be mistakenly activated whenever you cmd+tab away from the window, you can map it back to ctrl with the settings icon
  - if a popup (for example asking you to confirm quitting a proof) is unresponsive, hit tab multiple times until the buttons are selected, then hit enter to select one of them
- if emacs pvs inside the image is not recognizing any libraries, you need to update the path
- use the command `source setpvs.sh` 
  - the file should contain:
    ```shell
    export PVS_DIR=$HOME/pvs/pvs-7.1.0
    export PVS_LIBRARY_PATH=$PVS_DIR/nasalib
    ```
  ```bash
  rm .pvscontext
  cd pvsbin/
  rm *.bin
  
  
  proveit -C
  
  
  ./cleanbin-all 
  # (inside nasalib)
  ```
# Using dL in PVS
## First do this
- go through the useful resources page
- watch the intro video
- read some documentation and papers about PVS and dL (See 
- ask Tanner for his paper about dL, its super useful
## Intro to PVS
- turnstile: `|---------------------`
- Propositional Logic: if, and, or, etc
- LEMMA: thing you need to prove
- above the turnstile : ALL IS TRUE (AND) (antecedent)
- below the turnstile : one is true ALWAYS (OR) (consequent)
### Variables and Constants
- Constants can be defined as PVS variables like so, and must be referenced with a `cnst( )` around them

`x: VAR real`

- Variables are defined as natural numbers with UNIQUE arbitrary values that correspond to their index, and must be referenced with a `val( )` around them

`x: nat = 0`

## Writing things in PVS and dL
- [`IMPORTING dL@top`](https://github.com/n-crespo/NASA-2023/blob/master/pages/IMPORTING.md)
- [`DIFF()`](https://github.com/n-crespo/NASA-2023/blob/master/pages/DIFF.md): 
- [`LEMMA`](https://github.com/n-crespo/NASA-2023/blob/master/pages/lemma.md) 
- [`UNION()`](https://github.com/n-crespo/NASA-2023/blob/master/pages/UNION.md) 
- [`IFTE()`](https://github.com/n-crespo/NASA-2023/blob/master/pages/IFTE.md) 
- [`(BETA)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/BETA.md)
- [`TEST()`](https://github.com/n-crespo/NASA-2023/blob/master/pages/test.md)
- [`div_safe_re()`](https://github.com/n-crespo/NASA-2023/blob/master/pages/pages/div_safe_re.md) 
- [`SEQ(P, HP)` ](https://github.com/n-crespo/NASA-2023/blob/master/pages/SEQ.md) 
- [`STAR(ag)` ](https://github.com/n-crespo/NASA-2023/blob/master/pages/STAR.md) 
- [`^^`](https://github.com/n-crespo/NASA-2023/blob/master/pages/exponentiation.md): 
- [`ALLRUNS(DIFF(), postcondition)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/ALLRUNS.md)
- [`SOMERUNS(DIFF(), postcondition)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/SOMERUNS.md)
## Proving things in PVS and dL
### Miscellaneous
- [`(inst)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/inst.md)
- [`(skolem)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/skolem.md)
- [`(skeep)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/skeep.md)
- [`(flatten)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/flatten.md)
- [`(split)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/)
- [`(expand)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/expand.md)
- [`(iff)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/iff.md)
- [`(replaces)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/replaces.md)
- [`(skoletin)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/skoletin.md)
### Simplification
- [`(prop)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/prop.md)
- [`(bddsimp)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/bddsimp.md)
- [`(assert)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/assert.md)
- [`(ground)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/ground.md)
- [`(smash)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/smash.md)
- [`(grind)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/grind.md)
- [`(metit)`](https://github.com/n-crespo/NASA-2023/blob/master/metit.md)
### Utilities
- [`(help)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/help.md)
- [`(lemma)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/lemma.md)
- [`(quit)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/quit.md)
- [`(undo)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/undo.md)
- [`(hide)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/hide.md)
- [`(postpone)`](https://github.com/n-crespo/NASA-2023/blob/master/postpone.md)
### dL Commands
- See `dynamic_logic.pvs` for definitions and `Glossary_Plaidypvs.pvs` for examples  
- [`(<command>b)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/box.md)
- [`(<command>d)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/diamond.md)
- [`(dl-loop)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/loop.md)
- [`(dl-solve)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/solve.md)
- [`(dl-subs)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/sub.md)
- [`(dl-composeb)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/compose.md)
- [`(dl-flatten)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/flatten.md)
- [`(dl-ghost)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/ghosts.md)
- [`(dl-diffghost)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/diffghost.md)
- [`(dl-diffinv)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/diffinv.md)
- [`(dl-inst)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/inst.md)
- [`(dl-grind)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/dl-grind.md)
- [`(dl-diffcase)`](https://github.com/n-crespo/NASA-2023/blob/master/pages/diffcase.md)
- [`DLEXISTSRf`](https://github.com/n-crespo/NASA-2023/blob/master/pages/DLEXISTSRf.md)

## Differential Equations, Ghosts and Invariants
- most differential equations are impossible to solve
- solving ODE's will often make them more complicated then necessary
  - discrete ghost `(dl-ghost)` 
    - extra variable introduced to a proof to analyze the model
    - remember the value of a new variable in an old state for analyzing the change of an expression
    - discrete variable y which remembers the value of e (fresh)
    - Fresh Variables = new variable that doesn't affect main function
- differential ghosts:
  - evolve over time
  - extra variable added with a made up differential equation to analyze the system
  - increase complexity of the system
  - change the differential equation itself
  - (auxiliary variables) added to make the proof more conclusive, don't really exist
- `diff-ghost`: 
  - you are trying to prove x is always positive (it approaches 0 as it reaches infinity)
  - you introduce a new equation: $y' = y/2$
  - then you can say that `x*y^2=1`
  - why? because $y^2$ is always positive, so anything that x is must also be positive
  - y acts as a counterweight, always lifting x just enough to remain positive
  - my questions:
    - how do you figure out what y should equal?
      - GO BACKWARDS
      - we know that you have to use `diffinv` right after you introduce the ghost, so do that and have an unkown j(x) as the ghost
      - you should end up with an equation that = 0, so find the ghost expression that can satisfy it
      - THATS IT
    - how can you know for sure that `xy^2=1` ?
      - that is just a property of any positive number $(x)$ , use some reasoning to find small expressions like that that work for all numbers so you can build ghost variables around them
    - the new function must exist for as long as or longer than the original function that you are reasoning about
- `(dl-diffinv)`
  - use this after `diffghost`
  - when you have a Hybrid Program and something you want to prove is true (the HP would define the movement of the variable in the equation), differentiate the equation (and make sure to use values like x', y', etc) and plug in the values that you know those primes are equal to (from the HP definition)
  - you should get stuff that cancels out !!
  - (or rather an equation that equals 0)
- useful graphic:
  - Below: the differential ghost equation acts as a counterweight to f(x), ensuring that $xy^2 = 1$ will always be true, proving that x must always be positive
  - ![image_1687872581667_0.png](https://github.com/n-crespo/NASA-2023/blob/master/assets/image_1687872581667_0_1688677124071_0.png)

## Off-Topic Math
- Random slightly off-topic math:
  - you can define real numbers as the set of all lowest upper bounds of all nonempty, ___ sets
    - for example, take the set:
      - $x^2 <= 2$  and assume x is a rational number
      - the $lub$ , or lowest upper bound, is $sqrt(2)$
  - also, like everything in math can be described using limits,
    - ex. the double ^^ is just the x^^a = limit of x^^q as q approaches A
  - also rational numbers (or reals i think(?)) are like 0% of all numbers
    - if you took a random number there's a 0% chance it would be rational (or real) (i forgot)
    - they also have lots of holes in them, namely irrational numbers like $sqrt(2)$ and $pi$
$x^2$
# KeYmaera
- see [KeYmaera](https://github.com/n-crespo/NASA-2023/blob/master/pages/keymaera.md)
- see [KeYmaera](/pages/keymaera.md)
