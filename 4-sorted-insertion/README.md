# 4 Sorted Insertion

## Keeping Order

Well, apparently, putting everything randomly into one place, one List, one Pile, one Box, is not always ideal. We can save a lot of time if we have order in our items.

In Germany, we say:
> Wer Ordnung hält, ist nur zu faul zum Suchen.

(Who's tidy is just too lazy to search)

This applies perfectly to tidy Data Structures!

But sorting the whole collection every time we've added one item sounds crazy. What we'd need is a Data Structure that allows us to more easily maintain the order. If you spill a cup of coffee, you would not start cleaning the whole apartment, right?

What we need, is a method that allows us to keep our sorted collection sorted.

## Sorted Insertion

Turns out, this is not so hard. I will spare you the details, but we can simply:
- Use Binary Search to find the item that we want to insert.
- If we find an item with the same value, just put our item right behind it.
- If we don't, put it where we last searched for it.

e.g.:
- given: `3, 5, 7, 9, 11`
- we search for `4` and first in the middle (`7`)
- it's smaller, so we look in the left half's (`3, 5`) middle (`3`)
- it's greater, so we look in the right half's (`5`) middle (`5`)
- it's smaller, the collection is empty now, so we insert it left of `5`:
- `3, 4, 5, 7, 9, 11`

### Complexity
- Search: Binary Search O(log2 n)
- Insert: 
  - LinkedList: O(1) - because we just need to re-link two nodes.
  - Array: O(n) - because we need to move all items on the right away.

=> Complexity: O(n)

Darnit. We were so efficient at finding the right place, but we lose the whole advantage because of moving stuff around when making space.

Could there be a better Data Structure for this?
- The answer is yes, but more on that, next week

## Bonus Exercise
- Make a class named `SortedList<T>`
- When inserting items, put them in the right place right away