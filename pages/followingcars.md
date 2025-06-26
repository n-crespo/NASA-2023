# Following Cars

```py
ArchiveEntry "Following Cars"

Definitions
    Real va;
End.

ProgramVariables
    Real xb;
    Real xa;
    Real d;
End.

Problem
    (xa > 0) &
    (xa > xb)
->
    [{xa' = va}
    {xb' = (xa-xb)/2}

] (xa>xb)

End.
End.
```

- This Hybrid Program describes 2 cars, A in front, and B behind, which follow
  each other. The velocity of A is constant, while the velocity of B is constantly
  reassigned to half of the distance between A and B, gradually getting smaller.
  The distance between the two cars will become infinitely small, but they will
  never touch.
