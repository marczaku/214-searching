# 1 Linear Search
The most obvious Solution and also implemented by Static and Dynamic Arrays and any other Collection that does not provide special functionality for Searching:

Iterate over every Element and check each item, whether it matches the condition. If it does, stop the iteration and return the given item.

<details>
  <summary>Pseudo-Code</summary>

```
procedure linear_search (list, value)

   for each item in the list
      if match item == value
         return the item's location
      end if
   end for
   return item_not_found
end procedure
```

</details>

## Complexity

Well, what could Linear Search's Complexity be? Exactly!
- O(n) (Linear)

For a size of `n`, in worst case, we need to compare each of the `n` items.\

Does it matter, whether we search from the Front or the Back?
- Yes and No. It depends on whether you want to have the first or last Element satisfying the condition. But usually, the item is just as likely to be found in the beginning as in the end as in the middle.

That's why often, two Linear Search methods are provided. Like `IndexOf` and `LastIndexOf`.

Is this a good Algorithm?
Well, first of all, it scales really badly, If you have 10.000 items, it needs to run up to 10.000 checks. But as long as the collection is not too large, or you don't need to search something too often, it's absolutely fine.

Other techniques to reduce the complexity include:
- Sorting (costs extra performance preparing, only worth it if you search a lot)
- Hashing (costs extra memory and a small bit of performance, worth it, if you can afford)
- Caching (extra effort programming, harder to refactor, but if you don't need to find something AGAIN, that's great)