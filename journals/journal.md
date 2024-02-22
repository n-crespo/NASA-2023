This needs to be merged.

## Attempt 1

Consider this equation: 

$$ a = A * (2 * \frac {x-b}{2b}) $$

If we assume x starts at 20 and b is at 10, 

$$ a = A * (2 * \frac {20-10}{2*10}) $$
$$ a = A * (2 * \frac {10}{20}) $$
$$ a = A * (2 * \frac {10}{20}) $$
$$ a = A * (2 * \frac {1}{2}) $$
$$ a = A $$


If we assume x starts at 50 and b is at 10,

$$ a = A * ( 2 * \frac {50-10}{2*10})$$
$$ a = A * ( 2 * \frac {40}{20})$$
$$ a = A * ( 2 * 2)$$

Conclusion: The above does not work. 

## Attempt 2

Consider this other equation

$$ a = A * \frac {|x-b|}{x-b|} $$


This should work. Whenever x is above b, a will be A, when it is below b it will
be -A. When x is at b, A will be 0 / 0... Which isn't great. Depending on
