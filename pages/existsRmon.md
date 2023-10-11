-
  > Existential monotonicity in succedent: replace `p(x)` with a characteristic property `q(x)`.  
-
  ```
  Use:                      Show:
  G |- \exists x q(x), D    G, q(x) |- p(x), D
  -------------------------------------------- M∃R
  G |- \exists x p(x), D
  ```
- If there exists an x that maintains a post condition $p(x)$ , then you can say that it also suggests a postcondition $q(x)$ , but only if $q(x)$ itself makes $p(x)$ true
- this is a [[Tactic]] in [[KeYmaera]] but does not exist as a proof rule (as far as i know) in [[dL]]
  id:: 64b6d078-6dba-49ec-bc54-5f98f38fddab
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
	- see `dynamic_logic.pvs` under `%% GENERALIZE`
- #exists #SOMERUNS #diamond #KeYmaera
- ## What Tanner said about [[existsrMon]]
	- just use `inst()` or `instt()`, they should both work #inst #instantiation #instt
	-
