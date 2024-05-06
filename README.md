# 203 Searching

## Introduction

Now, after looking at sorting, we are ready ro return to searching. This chapter assumes that we have a simple collection in which items have an order and can be accessed via their indices.

This knowledge, you will be able to apply whenever you need to find an item matching a certain criteria.

You will understand the performance impact that searching will have and how you can reduce the impact.

## Problem
We need to find the first item that matches a condition in a collection.
- list simply refers to a sequential container type
- the actual data type does not matter
- e.g. Static Array, List, Linked List
We have an equality function `F` that defines whether on element matches the one being searched
- it returns `true`, if it matches
- and `false`, if it does not

Example:
- we have: `red`, `orange`, `white`, `green`, `blue`
- `F` is defined as: Color does not contain RED component
- result: `green`

## Use Case
Anything, really: 
- Find the next available Quest
- Find the position of a Player
- Find The GameManager-Class
- Find the correct Translation of a UI Text
- Find the Path Separator `/` in an URL
- Find the lowest Health Character
- Find a certain Card in a Card Pile.

## Passing Criteria
- Implement a Binary Search Algorithm
- Write Unit Tests

## Excellent Criteria
- Measure its efficiency
- Compare it to Linear Search

## Bonus: Implement Sorted List