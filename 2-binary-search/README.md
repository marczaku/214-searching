# 2 Binary Search

 There's a better way of finding an item. Under a certain condition.

## Let's Play A Game

 - I pick a number between 1 and 100.
 - You guess the number.
 - I tell you, whether my number is less than or greater than your guess.
 - We continue, until you find the correct number.
 - How many tries do you need?

## Prerequisites

- Not only the equality Function `F`, but also a comparison Operator `R` is needed.
- The collection needs to be sorted by `R`

Now, we can apply the same strategy of the Number Guessing Game:
- Go to the middle element
- If it is the wanted item -> bingo!
- If not, use the comparison Operator to find out, whether the searched item is in the lower or higher half of the collection
- Repeat in the remaining half
- Make sure to stop, if you've run out of items and could not find it :)

<details>
  <summary>Pseudo-Code</summary>

```
Procedure binary_search
   A ← sorted array
   n ← size of array
   x ← value to be searched

   Set lowerBound = 0
   Set upperBound = n-1 

   while x not found
      if upperBound < lowerBound 
         return -1: x does not exists.
   
      set midPoint = (lowerBound + upperBound) / 2
      
      if A[midPoint] < x
         set lowerBound = midPoint + 1
      else if A[midPoint] > x
         set upperBound = midPoint - 1
      else if A[midPoint] = x
         return midPoint: x found at location midPoint
      end if
   end while
   
end procedure
```

</details>

### Complexity

So, we half the size of the problem and then we half it again and again and again. How many of you remember from Intermediate Grade Math Classes, what function / expression expresses this?

Exponent:
- 2^0 = 1
- 2^1 = 2
- 2^2 = 2*2 = 4
- 2^3 = 2*2*2 = 8
- 2^n = 2*2*...2 (1 n times multiplied with 2)

Negative component:
- 2^-1 = 1/2 = 0.5
- 2^-2 = 1/2/2 = 1/4 = 0.25
- 2^-3 = 1/2/2/2 = 1/8 = 0.125
- 2^-n = 1/2/...2 (1 n times divided by 2)

Logarithm:
- log2 1 = 0
- log2 2 = 1
- log2 4 = 2
- log2 8 = 3
- log2 n = The exponent of 2 to give n

Or, to phrase it more approachably: How many times 8 can be divided by two.

Oh, that's interesting. How many times 8 can be divided by two. Isn't that also, what Binary Search does? Divide a problem by two for as many times as necessary?

That's why Binary Search's Complexity is:
- O(log2 n) (logarithmic)

How good is that? Turns out extremely good:
- log2 1000 = ~10
- log2 2000 = ~11
- log2 1,000,000 = ~20
- log2 2,000,000 = ~21

As you can see, whenever the problem size doubles, the complexity only increases by one. Nice.

### When to Use?
When you need to find items regularly and can not afford the extra memory that Hashing requires. Also, if the items come sorted, anyways.
