DIFF
====
- describe a [Hybrid Programs](pages/HybridPrograms.md) (with only first order differential equations)
- ex. `dyn : HP = DIFF( (: (x,val(x)) :))`
- dyn stands for dynamics, thing on other side of colon describes type of object (in this case HP = hybrid program)
- everything inside function must be inside `(: (a, b), (c, d) :)` <-- list
- `(x, val(x))`: ordered pair meaning $x' = x$
