# Bang Bang Controller

- This scenario depicts 1 car trying to reach a target velocity of `tv`.
  However, it uses a clunky controller that means that it can only change its
  velocity by `A`, a positive integer, or `-A`, which is negative.
- In this case, the car has a checking mechanism that checks the position of the
  car compared to a target position. The controller can then change the velocity
  (or acceleration in some examples) to `A` or `-A`, and then continues moving.
  The controller checks again only after `tau` seconds. The idea is that the
  object is forever oscillating around a target position, but never getting to
  far away from it.
