# existsrMon

> Existential monotonicity in succedent: replace `p(x)` with a characteristic
> property `q(x)`.

```text
Use:                      Show:
G |- \exists x q(x), D    G, q(x) |- p(x), D
-------------------------------------------- M∃R
G |- \exists x p(x), D
```

- If there exists an x that maintains a post condition $p(x)$ , then you can say
  that it also suggests a postcondition $q(x)$ , but only if $q(x)$ itself makes
  $p(x)$ true
- this is a Tactic in KeYmaera but does not exist as a proof rule (as far as i
  know) in [dL](../pages/dL.md)
- potential alternatives include:

  - **`dl-mono`**
    - `dl-MbL`
    - `dl-MbR`
  - **`dl-monod`**
    - `dl-MdR`
    - `dl-MdL`
  - `dl-MdR`
  - `dl-MEbR`
  - `dl-MEbRA`
  - see `dynamic_logic.pvs`

## What Tanner said about `existsrMon`

- just use `inst()` or `instt()`, they should both work
