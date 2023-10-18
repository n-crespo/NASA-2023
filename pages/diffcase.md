Differential Case
=================
- IF the precondition matches the post condition AND the Hybrid Program does NOT affect the variables in each of the conditions, the ENTIRE HP can be removed
	- this can be utilized when PVS does not recognize the value of a variable when it is very far down a certain branch
	- used to ensure the (constant) variable's value is explicitly defined for longer
- instantiate a few expressions (usually ones that are already in the antecedent) so that dL can recognize them later on
- used in `dl_cooling`
- similar to KeYmaera's [existsRmon](../pages/existsRmon.md)
- same thing as dL's [Differential Cut](../pages/DifferentialCut.md), which is also in KeYmaera
